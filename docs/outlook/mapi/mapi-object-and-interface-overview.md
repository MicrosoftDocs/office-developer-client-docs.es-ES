---
title: Información general sobre el objeto MAPI y la interfaz
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
# <a name="mapi-object-and-interface-overview"></a><span data-ttu-id="67120-103">Información general sobre el objeto MAPI y la interfaz</span><span class="sxs-lookup"><span data-stu-id="67120-103">MAPI Object and Interface Overview</span></span>

  
  
<span data-ttu-id="67120-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67120-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67120-105">Un objeto MAPI es una clase de objeto C++ o una estructura de datos C heredada de una o más interfaces MAPI, o colecciones de funciones relacionadas.</span><span class="sxs-lookup"><span data-stu-id="67120-105">A MAPI object is a C++ object class or C data structure inherited from one or more MAPI interfaces, or collections of related functions.</span></span> <span data-ttu-id="67120-106">Estas colecciones de funciones relacionadas son conocidas por los desarrolladores de C++ como funciones virtuales puras.</span><span class="sxs-lookup"><span data-stu-id="67120-106">These collections of related functions are known to C++ developers as pure virtual functions.</span></span> <span data-ttu-id="67120-107">Para una función virtual pura, MAPI proporciona solo el prototipo de función, no una implementación.</span><span class="sxs-lookup"><span data-stu-id="67120-107">For a pure virtual function, MAPI supplies only the function prototype, not an implementation.</span></span> <span data-ttu-id="67120-108">Se espera que una aplicación cliente, un proveedor de servicios o MAPI proporcione esta implementación mediante la creación de una clase de objeto que hereda de la interfaz y se ajusta a las descripciones de funciones de la API de mensajería.</span><span class="sxs-lookup"><span data-stu-id="67120-108">It is expected that a client application, a service provider, or MAPI will provide this implementation by creating an object class that inherits from the interface and conforms to the function descriptions of the Messaging API.</span></span> <span data-ttu-id="67120-109">Solo se puede crear una instancia de una interfaz MAPI a través de una clase heredada.</span><span class="sxs-lookup"><span data-stu-id="67120-109">A MAPI interface can be instantiated only through an inherited class.</span></span>
  
<span data-ttu-id="67120-110">Hay muchos objetos MAPI diferentes, cada objeto que hereda de una interfaz que finalmente se hereda de la [interfaz IUnknown.](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67120-110">There are many different MAPI objects, each object inheriting from an interface that is ultimately inherited from the [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="67120-111">**IUnknown es** la interfaz base del Modelo de objetos componentes OLE (COM).</span><span class="sxs-lookup"><span data-stu-id="67120-111">**IUnknown** is the OLE Component Object Model (COM) base interface.</span></span> <span data-ttu-id="67120-112">Proporciona a los objetos MAPI un mecanismo estándar para la comunicación y el control.</span><span class="sxs-lookup"><span data-stu-id="67120-112">It provides MAPI objects with a standard mechanism for communication and control.</span></span> <span data-ttu-id="67120-113">COM determina cómo los implementadores de objetos controlan problemas como la administración de memoria, la administración de parámetros y el multithreading.</span><span class="sxs-lookup"><span data-stu-id="67120-113">COM dictates how object implementers handle issues such as memory management, parameter management, and multithreading.</span></span> <span data-ttu-id="67120-114">Al cumplir con este modelo, un implementador de objetos se adhiere a un contrato según lo especificado por las interfaces incluidas en el objeto.</span><span class="sxs-lookup"><span data-stu-id="67120-114">By conforming to this model, an object implementer adheres to a contract as specified by the interfaces included in the object.</span></span> 
  
<span data-ttu-id="67120-115">Muchas interfaces MAPI se heredan directamente de **IUnknown,** mientras que otras se heredan indirectamente a través de una de las otras dos interfaces base: [IMAPIProp : IUnknown](imapipropiunknown.md) para la administración de propiedades e [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) para el acceso a carpetas y libretas de direcciones.</span><span class="sxs-lookup"><span data-stu-id="67120-115">Many MAPI interfaces are inherited directly from **IUnknown**, while others are inherited indirectly through one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) for property management and [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) for folder and address book access.</span></span> <span data-ttu-id="67120-116">Las interfaces base nunca se implementan como objetos independientes; siempre se implementan como parte de otros objetos, objetos que implementan interfaces derivadas.</span><span class="sxs-lookup"><span data-stu-id="67120-116">Base interfaces are never implemented as separate, standalone objects; they are always implemented as part of other objects, objects that implement derived interfaces.</span></span> 
  
<span data-ttu-id="67120-117">MAPI define muchos tipos de objetos, cada uno implementado por uno o más componentes MAPI.</span><span class="sxs-lookup"><span data-stu-id="67120-117">MAPI defines many types of objects, each implemented by one or more MAPI components.</span></span> <span data-ttu-id="67120-118">Mapi, los proveedores de servicios y los componentes de formulario personalizados usan los objetos implementados por los clientes.</span><span class="sxs-lookup"><span data-stu-id="67120-118">Objects implemented by clients are used by MAPI, by service providers, and by custom form components.</span></span> <span data-ttu-id="67120-119">Los objetos implementados por los proveedores de servicios normalmente los usan MAPI y los clientes.</span><span class="sxs-lookup"><span data-stu-id="67120-119">Objects implemented by service providers are typically used by MAPI and by clients.</span></span> <span data-ttu-id="67120-120">Otros componentes de formularios y clientes usan objetos implementados por proveedores de bibliotecas de formularios y servidores de formularios.</span><span class="sxs-lookup"><span data-stu-id="67120-120">Objects implemented by form library providers and form servers are used by other form components and by clients.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="67120-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="67120-121">See also</span></span>



[<span data-ttu-id="67120-122">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="67120-122">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="67120-123">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="67120-123">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="67120-124">Conceptos de MAPI</span><span class="sxs-lookup"><span data-stu-id="67120-124">MAPI Concepts</span></span>](mapi-concepts.md)

