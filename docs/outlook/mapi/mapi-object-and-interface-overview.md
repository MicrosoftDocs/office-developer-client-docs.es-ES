---
title: Introducción a la interfaz y el objeto MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fcd85bf518f4e6466bf15a09e417767bc34df78d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345790"
---
# <a name="mapi-object-and-interface-overview"></a><span data-ttu-id="35359-103">Introducción a la interfaz y el objeto MAPI</span><span class="sxs-lookup"><span data-stu-id="35359-103">MAPI Object and Interface Overview</span></span>

  
  
<span data-ttu-id="35359-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35359-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35359-105">Un objeto MAPI es una clase de objeto de C++ o una estructura de datos de C heredada de una o varias interfaces MAPI o colecciones de funciones relacionadas.</span><span class="sxs-lookup"><span data-stu-id="35359-105">A MAPI object is a C++ object class or C data structure inherited from one or more MAPI interfaces, or collections of related functions.</span></span> <span data-ttu-id="35359-106">Estas colecciones de funciones relacionadas son conocidas para los programadores de C++ como funciones virtuales puras.</span><span class="sxs-lookup"><span data-stu-id="35359-106">These collections of related functions are known to C++ developers as pure virtual functions.</span></span> <span data-ttu-id="35359-107">Para una función virtual pura, MAPI proporciona solo el prototipo de función, no una implementación.</span><span class="sxs-lookup"><span data-stu-id="35359-107">For a pure virtual function, MAPI supplies only the function prototype, not an implementation.</span></span> <span data-ttu-id="35359-108">Se espera que una aplicación cliente, un proveedor de servicios o MAPI proporcionen esta implementación mediante la creación de una clase de objeto que herede de la interfaz y que se ajuste a las descripciones de las funciones de la API de mensajería.</span><span class="sxs-lookup"><span data-stu-id="35359-108">It is expected that a client application, a service provider, or MAPI will provide this implementation by creating an object class that inherits from the interface and conforms to the function descriptions of the Messaging API.</span></span> <span data-ttu-id="35359-109">Una interfaz MAPI sólo se puede instanciar a través de una clase heredada.</span><span class="sxs-lookup"><span data-stu-id="35359-109">A MAPI interface can be instantiated only through an inherited class.</span></span>
  
<span data-ttu-id="35359-110">Hay muchos objetos MAPI diferentes, cada uno de los objetos que hereda de una interfaz que se hereda en última instancia desde la interfaz [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="35359-110">There are many different MAPI objects, each object inheriting from an interface that is ultimately inherited from the [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="35359-111">**IUnknown** es la interfaz base del modelo de objetos componentes (com) OLE.</span><span class="sxs-lookup"><span data-stu-id="35359-111">**IUnknown** is the OLE Component Object Model (COM) base interface.</span></span> <span data-ttu-id="35359-112">Proporciona objetos MAPI con un mecanismo estándar para la comunicación y el control.</span><span class="sxs-lookup"><span data-stu-id="35359-112">It provides MAPI objects with a standard mechanism for communication and control.</span></span> <span data-ttu-id="35359-113">COM indica cómo los implementadores de objetos controlan problemas como la administración de memoria, la administración de parámetros y el subprocesamiento múltiple.</span><span class="sxs-lookup"><span data-stu-id="35359-113">COM dictates how object implementers handle issues such as memory management, parameter management, and multithreading.</span></span> <span data-ttu-id="35359-114">Mediante la conformidad con este modelo, un implementador de objetos se adhiere a un contrato según se especifica en las interfaces incluidas en el objeto.</span><span class="sxs-lookup"><span data-stu-id="35359-114">By conforming to this model, an object implementer adheres to a contract as specified by the interfaces included in the object.</span></span> 
  
<span data-ttu-id="35359-115">Muchas interfaces MAPI se heredan directamente de **IUnknown**, mientras que otras se heredan indirectamente a través de una de las otras dos interfaces base: [IMAPIProp: IUnknown](imapipropiunknown.md) para la administración de propiedades y [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) para Folder y acceso a la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="35359-115">Many MAPI interfaces are inherited directly from **IUnknown**, while others are inherited indirectly through one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) for property management and [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) for folder and address book access.</span></span> <span data-ttu-id="35359-116">Las interfaces base no se implementan nunca como objetos independientes independientes; siempre se implementan como parte de otros objetos, objetos que implementan interfaces derivadas.</span><span class="sxs-lookup"><span data-stu-id="35359-116">Base interfaces are never implemented as separate, standalone objects; they are always implemented as part of other objects, objects that implement derived interfaces.</span></span> 
  
<span data-ttu-id="35359-117">MAPI define muchos tipos de objetos, cada uno de ellos implementado por uno o varios componentes de MAPI.</span><span class="sxs-lookup"><span data-stu-id="35359-117">MAPI defines many types of objects, each implemented by one or more MAPI components.</span></span> <span data-ttu-id="35359-118">MAPI, los proveedores de servicios y los componentes de formulario personalizados usan los objetos que implementan los clientes.</span><span class="sxs-lookup"><span data-stu-id="35359-118">Objects implemented by clients are used by MAPI, by service providers, and by custom form components.</span></span> <span data-ttu-id="35359-119">MAPI y los clientes suelen usar los objetos implementados por los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="35359-119">Objects implemented by service providers are typically used by MAPI and by clients.</span></span> <span data-ttu-id="35359-120">Los componentes de formularios y los clientes usan los objetos implementados por los proveedores de bibliotecas de formularios y los servidores de formularios.</span><span class="sxs-lookup"><span data-stu-id="35359-120">Objects implemented by form library providers and form servers are used by other form components and by clients.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="35359-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="35359-121">See also</span></span>



[<span data-ttu-id="35359-122">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35359-122">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="35359-123">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="35359-123">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="35359-124">Conceptos de MAPI</span><span class="sxs-lookup"><span data-stu-id="35359-124">MAPI Concepts</span></span>](mapi-concepts.md)

