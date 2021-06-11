---
title: MAPI y modelo de objetos componentes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a91ab8497a690fd4b99f76274d0213284253fd06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334471"
---
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="3c46d-103">MAPI y modelo de objetos componentes</span><span class="sxs-lookup"><span data-stu-id="3c46d-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="3c46d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c46d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c46d-105">La Windows SDK incluye una explicación completa de las reglas para implementar objetos que se ajustan al modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="3c46d-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="3c46d-106">Estas reglas abordan cómo hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3c46d-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="3c46d-107">Diseño de interfaces y objetos.</span><span class="sxs-lookup"><span data-stu-id="3c46d-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="3c46d-108">Implemente [la interfaz IUnknown.](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c46d-108">Implement the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="3c46d-109">Administrar la memoria.</span><span class="sxs-lookup"><span data-stu-id="3c46d-109">Manage memory.</span></span>
    
- <span data-ttu-id="3c46d-110">Controlar el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="3c46d-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="3c46d-111">Implemente objetos de subprocesos de apartamento.</span><span class="sxs-lookup"><span data-stu-id="3c46d-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="3c46d-112">Aunque todos los objetos MAPI se consideran basados en COM porque implementan interfaces que heredan de [IUnknown,](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)MAPI se desvía en algunas situaciones de las reglas COM estándar.</span><span class="sxs-lookup"><span data-stu-id="3c46d-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="3c46d-113">Esta desviación permite a los desarrolladores más flexibilidad en sus implementaciones.</span><span class="sxs-lookup"><span data-stu-id="3c46d-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="3c46d-114">Por ejemplo, una interfaz MAPI, como cualquier interfaz COM, describe un contrato entre el implementador y el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="3c46d-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="3c46d-115">Una vez creada y publicada la interfaz, su definición no puede ni cambia.</span><span class="sxs-lookup"><span data-stu-id="3c46d-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="3c46d-116">MAPI no se desvía de esta descripción, pero relaja un poco la descripción.</span><span class="sxs-lookup"><span data-stu-id="3c46d-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="3c46d-117">Los implementadores pueden optar por no implementar métodos concretos, devolviendo uno de los siguientes valores de error al autor de la llamada:</span><span class="sxs-lookup"><span data-stu-id="3c46d-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="3c46d-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="3c46d-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="3c46d-119">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="3c46d-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="3c46d-120">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="3c46d-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="3c46d-121">MAPI_E_TYPE_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="3c46d-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="3c46d-122">Las demás desviaciones de las reglas COM estándar se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3c46d-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="3c46d-123">**Regla de programación COM**</span><span class="sxs-lookup"><span data-stu-id="3c46d-123">**COM programming rule**</span></span>|<span data-ttu-id="3c46d-124">**Variación MAPI**</span><span class="sxs-lookup"><span data-stu-id="3c46d-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3c46d-125">Todos los parámetros de cadena de los métodos de interfaz deben ser Unicode.</span><span class="sxs-lookup"><span data-stu-id="3c46d-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="3c46d-126">Las interfaces MAPI se definen para permitir parámetros de cadena Unicode o ANSI.</span><span class="sxs-lookup"><span data-stu-id="3c46d-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="3c46d-127">Muchos métodos que tienen un parámetro string también tienen **un parámetro ulFlags;** el ancho de un parámetro de cadena se indica mediante el valor de la marca MAPI_UNICODE en **ulFlags**.</span><span class="sxs-lookup"><span data-stu-id="3c46d-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="3c46d-128">Algunas interfaces MAPI no admiten Unicode y devuelven MAPI_E_BAD_CHARWIDTH cuando se establece MAPI_UNICODE marca.</span><span class="sxs-lookup"><span data-stu-id="3c46d-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="3c46d-129">Todos los métodos de interfaz deben tener un tipo devuelto de HRESULT.</span><span class="sxs-lookup"><span data-stu-id="3c46d-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="3c46d-130">MAPI tiene al menos un método que devuelve un valor que no es HRESULT: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="3c46d-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="3c46d-131">Los autores de llamadas y los implementadores deben asignar y liberar memoria para los parámetros de interfaz mediante el uso de los asignadores de tareas COM estándar.</span><span class="sxs-lookup"><span data-stu-id="3c46d-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="3c46d-132">Todos los métodos MAPI usan los asignadores vinculados [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md) para administrar la memoria de los parámetros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="3c46d-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="3c46d-133">Todas las implementaciones MAPI de interfaces definidas por OLE, como [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), usan los asignadores de tareas COM estándar.</span><span class="sxs-lookup"><span data-stu-id="3c46d-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="3c46d-134">Todos los parámetros de puntero de salida deben establecerse explícitamente en NULL cuando se produce un error en un método.</span><span class="sxs-lookup"><span data-stu-id="3c46d-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="3c46d-135">Las interfaces MAPI requieren que los parámetros de puntero de salida se establezcan en NULL o no se cambien cuando se produce un error en un método.</span><span class="sxs-lookup"><span data-stu-id="3c46d-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="3c46d-136">Todas las implementaciones MAPI de interfaces definidas por OLE establecen explícitamente los parámetros en NULL en caso de error.</span><span class="sxs-lookup"><span data-stu-id="3c46d-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="3c46d-137">Implemente objetos agregables siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="3c46d-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="3c46d-138">Las interfaces MAPI no se pueden agregar.</span><span class="sxs-lookup"><span data-stu-id="3c46d-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3c46d-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c46d-139">See also</span></span>



[<span data-ttu-id="3c46d-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="3c46d-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="3c46d-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="3c46d-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="3c46d-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3c46d-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="3c46d-143">Introducción a la interfaz y el objeto MAPI</span><span class="sxs-lookup"><span data-stu-id="3c46d-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

