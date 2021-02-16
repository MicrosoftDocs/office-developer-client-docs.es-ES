---
title: Implementación de objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c0d67d10d54591de926724cbf594a44f17e9ea14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310174"
---
# <a name="implementing-mapi-objects"></a><span data-ttu-id="848b7-103">Implementación de objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="848b7-103">Implementing MAPI Objects</span></span>

  
  
<span data-ttu-id="848b7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="848b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="848b7-105">Los objetos MAPI se pueden implementar mediante clases C++ o estructuras de datos C, según el lenguaje y el conjunto de API que esté usando un cliente o proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="848b7-105">MAPI objects can be implemented by using C++ classes or C data structures, depending on the language and the API set a client or service provider is using.</span></span> <span data-ttu-id="848b7-106">Los proveedores de servicios se pueden escribir en C o C++ con la interfaz del proveedor de servicios MAPI; las aplicaciones cliente también pueden usar C o C++.</span><span class="sxs-lookup"><span data-stu-id="848b7-106">Service providers can be written in C or C++ with the MAPI service provider interface; client applications can also use C or C++.</span></span> <span data-ttu-id="848b7-107">Si es posible, los clientes y proveedores de servicios que usan la interfaz de programación orientada a objetos deben usar C++.</span><span class="sxs-lookup"><span data-stu-id="848b7-107">If possible, clients and service providers that use the object-oriented programming interface should use C++.</span></span> 
  
<span data-ttu-id="848b7-108">C++ es la opción preferida porque MAPI es una tecnología orientada a objetos y C++ se presta más fácilmente al desarrollo orientado a objetos.</span><span class="sxs-lookup"><span data-stu-id="848b7-108">C++ is the preferred choice because MAPI is an object-oriented technology, and C++ lends itself more readily to object-oriented development.</span></span> <span data-ttu-id="848b7-109">El código resultante es más sencillo y sencillo, lo que facilita el mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="848b7-109">The resulting code is simpler and more straightforward, making it easier to maintain.</span></span> <span data-ttu-id="848b7-110">La documentación mapi está escrita principalmente para desarrolladores de C++; todas las descripciones de sintaxis para los métodos de interfaz MAPI de esta referencia están en C++.</span><span class="sxs-lookup"><span data-stu-id="848b7-110">The MAPI documentation is written primarily for C++ developers; all of the syntax descriptions for the MAPI interface methods in this Reference are in C++.</span></span>
  
<span data-ttu-id="848b7-111">Los desarrolladores pueden usar microsoft Visual Studio y herramientas de desarrollo de terceros para desarrollar soluciones que llamen a MAPI.</span><span class="sxs-lookup"><span data-stu-id="848b7-111">Developers can use Microsoft Visual Studio and third-party development tools to develop solutions that call MAPI.</span></span> <span data-ttu-id="848b7-112">Tenga en cuenta que los desarrolladores deben usar C o C++no administrado, pero no C++ administrado para escribir soluciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="848b7-112">Note that developers should use C or unmanaged C++, but not managed C++ to write MAPI solutions.</span></span>
  
<span data-ttu-id="848b7-113">Cuando se implementa un objeto MAPI, un cliente o proveedor de servicios crea código para todos los métodos de interfaz, código para los métodos privados específicos de la implementación y código para admitir miembros de datos privados para mantener la información de estado.</span><span class="sxs-lookup"><span data-stu-id="848b7-113">When a MAPI object is implemented, a client or service provider creates code for all of the interface methods, code for any private methods that are specific to the implementation, and code to support private data members for maintaining state information.</span></span> <span data-ttu-id="848b7-114">El código de los métodos de interfaz debe seguir las especificaciones publicadas por MAPI que documentan el comportamiento esperado.</span><span class="sxs-lookup"><span data-stu-id="848b7-114">The code for the interface methods must follow the specifications published by MAPI that document expected behavior.</span></span> 
  
<span data-ttu-id="848b7-115">Hay muchas macros en el archivo de encabezado Mapidefs.h y archivos de encabezado OLE que los clientes y proveedores de servicios en cualquier idioma pueden usar para ayudarles con sus definiciones de objetos MAPI.</span><span class="sxs-lookup"><span data-stu-id="848b7-115">There are many macros in the Mapidefs.h header file and OLE header files that clients and service providers in either language can use to help them with their definitions of MAPI objects.</span></span> <span data-ttu-id="848b7-116">Por ejemplo, hay una macro para definir los métodos de cada una de las interfaces MAPI.</span><span class="sxs-lookup"><span data-stu-id="848b7-116">For example, there is a macro to define the methods of each of the MAPI interfaces.</span></span> <span data-ttu-id="848b7-117">La macro para definir los métodos de [la interfaz IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) aparece en Mapidefs.h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="848b7-117">The macro to define the methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface appears in Mapidefs.h as follows:</span></span> 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a><span data-ttu-id="848b7-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="848b7-118">See also</span></span>



[<span data-ttu-id="848b7-119">Información general sobre el objeto MAPI y la interfaz</span><span class="sxs-lookup"><span data-stu-id="848b7-119">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

