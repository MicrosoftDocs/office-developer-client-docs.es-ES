---
title: Implementar objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c0d67d10d54591de926724cbf594a44f17e9ea14
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397103"
---
# <a name="implementing-mapi-objects"></a><span data-ttu-id="a9b34-103">Implementar objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="a9b34-103">Implementing MAPI Objects</span></span>

  
  
<span data-ttu-id="a9b34-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9b34-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9b34-105">Objetos MAPI se pueden implementar mediante el uso de clases de C++ o C las estructuras de datos, dependiendo del lenguaje y la API de establece a un cliente o está usando el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="a9b34-105">MAPI objects can be implemented by using C++ classes or C data structures, depending on the language and the API set a client or service provider is using.</span></span> <span data-ttu-id="a9b34-106">Proveedores de servicios se pueden escribir en C o C++ con la interfaz de proveedor de servicio MAPI; También pueden usar las aplicaciones cliente de C o C++.</span><span class="sxs-lookup"><span data-stu-id="a9b34-106">Service providers can be written in C or C++ with the MAPI service provider interface; client applications can also use C or C++.</span></span> <span data-ttu-id="a9b34-107">Si es posible, los clientes y proveedores de servicios que usan la interfaz de programación orientada a objetos deben usar C++.</span><span class="sxs-lookup"><span data-stu-id="a9b34-107">If possible, clients and service providers that use the object-oriented programming interface should use C++.</span></span> 
  
<span data-ttu-id="a9b34-108">C++ es la opción preferida porque MAPI es una tecnología orientada a objetos y C++ se presta más fácilmente a desarrollo orientado a objetos.</span><span class="sxs-lookup"><span data-stu-id="a9b34-108">C++ is the preferred choice because MAPI is an object-oriented technology, and C++ lends itself more readily to object-oriented development.</span></span> <span data-ttu-id="a9b34-109">El código resultante es más sencilla y directa, haciendo que sea más fácil de mantener.</span><span class="sxs-lookup"><span data-stu-id="a9b34-109">The resulting code is simpler and more straightforward, making it easier to maintain.</span></span> <span data-ttu-id="a9b34-110">La documentación de MAPI está escrita principalmente para programadores de C++; todas las descripciones de sintaxis para los métodos de interfaz MAPI en esta referencia se encuentran en C++.</span><span class="sxs-lookup"><span data-stu-id="a9b34-110">The MAPI documentation is written primarily for C++ developers; all of the syntax descriptions for the MAPI interface methods in this Reference are in C++.</span></span>
  
<span data-ttu-id="a9b34-111">Los desarrolladores pueden usar Microsoft Visual Studio y herramientas de desarrollo de aplicaciones de terceros para desarrollar soluciones que llamar a MAPI.</span><span class="sxs-lookup"><span data-stu-id="a9b34-111">Developers can use Microsoft Visual Studio and third-party development tools to develop solutions that call MAPI.</span></span> <span data-ttu-id="a9b34-112">Tenga en cuenta que los desarrolladores deben utilizar C o C++ no administrado, pero no administran de C++ para escribir soluciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="a9b34-112">Note that developers should use C or unmanaged C++, but not managed C++ to write MAPI solutions.</span></span>
  
<span data-ttu-id="a9b34-113">Cuando se implementa un objeto MAPI, un proveedor de servicio o cliente crea código para todos los métodos de la interfaz, el código para los métodos privados que son específicos de la implementación y el código para admitir los miembros de datos privados para el mantenimiento de información de estado.</span><span class="sxs-lookup"><span data-stu-id="a9b34-113">When a MAPI object is implemented, a client or service provider creates code for all of the interface methods, code for any private methods that are specific to the implementation, and code to support private data members for maintaining state information.</span></span> <span data-ttu-id="a9b34-114">El código para los métodos de interfaz debe seguir las especificaciones publicadas por MAPI que documentar el comportamiento esperado.</span><span class="sxs-lookup"><span data-stu-id="a9b34-114">The code for the interface methods must follow the specifications published by MAPI that document expected behavior.</span></span> 
  
<span data-ttu-id="a9b34-115">Hay muchas macros en el archivo de encabezado Mapidefs.h y los archivos de encabezado OLE que pueden usar los clientes y proveedores de servicio en cualquier idioma para ayudarles con sus definiciones de objetos MAPI.</span><span class="sxs-lookup"><span data-stu-id="a9b34-115">There are many macros in the Mapidefs.h header file and OLE header files that clients and service providers in either language can use to help them with their definitions of MAPI objects.</span></span> <span data-ttu-id="a9b34-116">Por ejemplo, hay una macro para definir los métodos de cada una de las interfaces MAPI.</span><span class="sxs-lookup"><span data-stu-id="a9b34-116">For example, there is a macro to define the methods of each of the MAPI interfaces.</span></span> <span data-ttu-id="a9b34-117">La macro para definir los métodos de la interfaz [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) aparece en Mapidefs.h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="a9b34-117">The macro to define the methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface appears in Mapidefs.h as follows:</span></span> 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a><span data-ttu-id="a9b34-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9b34-118">See also</span></span>



[<span data-ttu-id="a9b34-119">Objeto MAPI e Introducción a la interfaz</span><span class="sxs-lookup"><span data-stu-id="a9b34-119">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

