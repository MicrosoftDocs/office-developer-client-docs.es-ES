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
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="d66fe-103">MAPI y modelo de objetos componentes</span><span class="sxs-lookup"><span data-stu-id="d66fe-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="d66fe-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d66fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d66fe-105">La documentación del SDK de Windows incluye una explicación completa de las reglas para implementar objetos que se ajustan al modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="d66fe-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="d66fe-106">Estas reglas abordan cómo hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d66fe-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="d66fe-107">Diseñe interfaces y objetos.</span><span class="sxs-lookup"><span data-stu-id="d66fe-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="d66fe-108">Implementar la interfaz [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d66fe-108">Implement the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="d66fe-109">Administrar la memoria.</span><span class="sxs-lookup"><span data-stu-id="d66fe-109">Manage memory.</span></span>
    
- <span data-ttu-id="d66fe-110">Controlar el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="d66fe-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="d66fe-111">Implementar objetos de subprocesamiento controlado.</span><span class="sxs-lookup"><span data-stu-id="d66fe-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="d66fe-112">Aunque todos los objetos MAPI se consideran basados en COM porque implementan interfaces que heredan de [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI se desvía en algunas situaciones de las reglas com estándar.</span><span class="sxs-lookup"><span data-stu-id="d66fe-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="d66fe-113">Esta desviación permite a los programadores más flexibilidad en sus implementaciones.</span><span class="sxs-lookup"><span data-stu-id="d66fe-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="d66fe-114">Por ejemplo, una interfaz MAPI, como cualquier interfaz COM, describe un contrato entre el implementador y el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d66fe-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="d66fe-115">Una vez que se ha creado y publicado la interfaz, su definición no puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="d66fe-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="d66fe-116">MAPI no se desvía de esta descripción, pero relaja ligeramente la descripción.</span><span class="sxs-lookup"><span data-stu-id="d66fe-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="d66fe-117">Los implementadores pueden elegir no implementar métodos en particular, devolver uno de los siguientes valores de error al autor de la llamada:</span><span class="sxs-lookup"><span data-stu-id="d66fe-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="d66fe-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="d66fe-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="d66fe-119">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="d66fe-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="d66fe-120">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d66fe-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="d66fe-121">MAPI_E_TYPE_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="d66fe-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="d66fe-122">Las demás desviaciones de las reglas estándar de COM se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d66fe-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="d66fe-123">**Regla de programación COM**</span><span class="sxs-lookup"><span data-stu-id="d66fe-123">**COM programming rule**</span></span>|<span data-ttu-id="d66fe-124">**Variante de MAPI**</span><span class="sxs-lookup"><span data-stu-id="d66fe-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d66fe-125">Todos los parámetros de cadena de los métodos de interfaz deben ser Unicode.</span><span class="sxs-lookup"><span data-stu-id="d66fe-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="d66fe-126">Las interfaces MAPI se definen para permitir los parámetros de cadena Unicode o ANSI.</span><span class="sxs-lookup"><span data-stu-id="d66fe-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="d66fe-127">Muchos de los métodos que tienen un parámetro de cadena también tienen un parámetro **ulFlags** ; el ancho de un parámetro de cadena se indica mediante el valor de la marca MAPI_UNICODE en **ulFlags**.</span><span class="sxs-lookup"><span data-stu-id="d66fe-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="d66fe-128">Algunas interfaces MAPI no admiten Unicode y devuelven MAPI_E_BAD_CHARWIDTH cuando se establece la marca MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d66fe-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="d66fe-129">Todos los métodos de interfaz deben tener un tipo de valor devuelto de HRESULT.</span><span class="sxs-lookup"><span data-stu-id="d66fe-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="d66fe-130">MAPI tiene al menos un método que devuelve un valor que no es HRESULT: [IMAPIAdviseSink:: Notify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="d66fe-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="d66fe-131">Los autores de llamadas e implementadores deben asignar y liberar memoria para los parámetros de interfaz mediante los asignadores de tareas COM estándar.</span><span class="sxs-lookup"><span data-stu-id="d66fe-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="d66fe-132">Todos los métodos de MAPI usan los asignadores vinculados [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md) para administrar la memoria para los parámetros de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="d66fe-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="d66fe-133">Todas las implementaciones MAPI de interfaces definidas por OLE, como [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), usan los asignadores de tareas com estándar.</span><span class="sxs-lookup"><span data-stu-id="d66fe-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="d66fe-134">Todos los parámetros de puntero de salida deben establecerse explícitamente en NULL cuando se produce un error en un método.</span><span class="sxs-lookup"><span data-stu-id="d66fe-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="d66fe-135">Las interfaces MAPI requieren que los parámetros de puntero se establezcan en NULL o que permanezcan inalterados cuando se produzca un error en un método.</span><span class="sxs-lookup"><span data-stu-id="d66fe-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="d66fe-136">Todas las implementaciones MAPI de interfaces definidas por OLE establecen explícitamente los parámetros de salida en NULL en caso de error.</span><span class="sxs-lookup"><span data-stu-id="d66fe-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="d66fe-137">Implemente objetos agregables siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="d66fe-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="d66fe-138">Las interfaces MAPI no son agregables.</span><span class="sxs-lookup"><span data-stu-id="d66fe-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d66fe-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d66fe-139">See also</span></span>



[<span data-ttu-id="d66fe-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="d66fe-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="d66fe-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="d66fe-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="d66fe-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d66fe-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="d66fe-143">Introducción a la interfaz y el objeto MAPI</span><span class="sxs-lookup"><span data-stu-id="d66fe-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

