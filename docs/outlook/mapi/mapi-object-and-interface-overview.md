---
title: Objeto MAPI e Introducción a la interfaz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fcd85bf518f4e6466bf15a09e417767bc34df78d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390992"
---
# <a name="mapi-object-and-interface-overview"></a><span data-ttu-id="fee7f-103">Objeto MAPI e Introducción a la interfaz</span><span class="sxs-lookup"><span data-stu-id="fee7f-103">MAPI Object and Interface Overview</span></span>

  
  
<span data-ttu-id="fee7f-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fee7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fee7f-105">Un objeto MAPI es una clase de objeto de C++ o C estructura de datos se hereda de una o más interfaces MAPI o colecciones de funciones relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fee7f-105">A MAPI object is a C++ object class or C data structure inherited from one or more MAPI interfaces, or collections of related functions.</span></span> <span data-ttu-id="fee7f-106">Estas colecciones de funciones relacionadas se conocen los desarrolladores de C++ como funciones virtuales puras.</span><span class="sxs-lookup"><span data-stu-id="fee7f-106">These collections of related functions are known to C++ developers as pure virtual functions.</span></span> <span data-ttu-id="fee7f-107">Para una función virtual pura, MAPI proporciona solo el prototipo de función, no una implementación.</span><span class="sxs-lookup"><span data-stu-id="fee7f-107">For a pure virtual function, MAPI supplies only the function prototype, not an implementation.</span></span> <span data-ttu-id="fee7f-108">Se espera que una aplicación cliente, un proveedor de servicios o MAPI proporcionará esta implementación mediante la creación de una clase de objeto que hereda de la interfaz y se ajusta a las descripciones de la función de la API de mensajería.</span><span class="sxs-lookup"><span data-stu-id="fee7f-108">It is expected that a client application, a service provider, or MAPI will provide this implementation by creating an object class that inherits from the interface and conforms to the function descriptions of the Messaging API.</span></span> <span data-ttu-id="fee7f-109">Una interfaz de MAPI se puede crear instancias sólo a través de una clase heredada.</span><span class="sxs-lookup"><span data-stu-id="fee7f-109">A MAPI interface can be instantiated only through an inherited class.</span></span>
  
<span data-ttu-id="fee7f-110">Hay muchos objetos MAPI diferentes, cada objeto que herede de una interfaz que se hereda en última instancia de la interfaz [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="fee7f-110">There are many different MAPI objects, each object inheriting from an interface that is ultimately inherited from the [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="fee7f-111">**IUnknown** es la interfaz base OLE componente modelo de objetos (COM).</span><span class="sxs-lookup"><span data-stu-id="fee7f-111">**IUnknown** is the OLE Component Object Model (COM) base interface.</span></span> <span data-ttu-id="fee7f-112">Proporciona objetos MAPI con un mecanismo estándar para la comunicación y control.</span><span class="sxs-lookup"><span data-stu-id="fee7f-112">It provides MAPI objects with a standard mechanism for communication and control.</span></span> <span data-ttu-id="fee7f-113">COM determina cómo los implementadores del objeto resolver problemas como la administración de memoria, la administración de parámetro y el subprocesamiento múltiple.</span><span class="sxs-lookup"><span data-stu-id="fee7f-113">COM dictates how object implementers handle issues such as memory management, parameter management, and multithreading.</span></span> <span data-ttu-id="fee7f-114">De forma que se ajusten a este modelo, un implementador de objeto se ajusta a un contrato tal como se especifica mediante las interfaces que se incluyen en el objeto.</span><span class="sxs-lookup"><span data-stu-id="fee7f-114">By conforming to this model, an object implementer adheres to a contract as specified by the interfaces included in the object.</span></span> 
  
<span data-ttu-id="fee7f-115">Muchas de las interfaces MAPI se heredan directamente de **IUnknown**, mientras que otras personas se heredan indirectamente a través de una de las otras dos interfaces bases: [IMAPIProp: IUnknown](imapipropiunknown.md) para la administración de propiedad y [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) para la carpeta y acceso a la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="fee7f-115">Many MAPI interfaces are inherited directly from **IUnknown**, while others are inherited indirectly through one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) for property management and [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) for folder and address book access.</span></span> <span data-ttu-id="fee7f-116">Interfaces base nunca se implementan como objetos independientes, de independiente; siempre se implementan como parte de otros objetos, los objetos que implementan interfaces derivan.</span><span class="sxs-lookup"><span data-stu-id="fee7f-116">Base interfaces are never implemented as separate, standalone objects; they are always implemented as part of other objects, objects that implement derived interfaces.</span></span> 
  
<span data-ttu-id="fee7f-117">MAPI define muchos tipos de objetos, cada uno implementado por uno o más componentes MAPI.</span><span class="sxs-lookup"><span data-stu-id="fee7f-117">MAPI defines many types of objects, each implemented by one or more MAPI components.</span></span> <span data-ttu-id="fee7f-118">Se utilizan objetos implementados por los clientes MAPI, proveedores de servicios y componentes de formularios personalizados.</span><span class="sxs-lookup"><span data-stu-id="fee7f-118">Objects implemented by clients are used by MAPI, by service providers, and by custom form components.</span></span> <span data-ttu-id="fee7f-119">Objetos que implementan los proveedores de servicio se usan normalmente por MAPI y por los clientes.</span><span class="sxs-lookup"><span data-stu-id="fee7f-119">Objects implemented by service providers are typically used by MAPI and by clients.</span></span> <span data-ttu-id="fee7f-120">Objetos implementan los proveedores de la biblioteca de formulario y los servidores de formulario se usan por otros componentes de formulario y por los clientes.</span><span class="sxs-lookup"><span data-stu-id="fee7f-120">Objects implemented by form library providers and form servers are used by other form components and by clients.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fee7f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="fee7f-121">See also</span></span>



[<span data-ttu-id="fee7f-122">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fee7f-122">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="fee7f-123">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fee7f-123">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="fee7f-124">Conceptos MAPI</span><span class="sxs-lookup"><span data-stu-id="fee7f-124">MAPI Concepts</span></span>](mapi-concepts.md)

