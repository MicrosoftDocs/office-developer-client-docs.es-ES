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
ms.openlocfilehash: cf687a7bfadb0981ca3440c2f81bc5de8f910924
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816574"
---
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="10193-103">MAPI y modelo de objetos componentes</span><span class="sxs-lookup"><span data-stu-id="10193-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="10193-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10193-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10193-105">La documentación del SDK de Windows incluye una explicación completa de las reglas para la implementación de objetos que se ajustan al modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="10193-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="10193-106">Estas reglas de direcciones cómo hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="10193-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="10193-107">Interfaces de diseño y objetos.</span><span class="sxs-lookup"><span data-stu-id="10193-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="10193-108">Implementar la interfaz [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="10193-108">Implement the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="10193-109">Administrar la memoria.</span><span class="sxs-lookup"><span data-stu-id="10193-109">Manage memory.</span></span>
    
- <span data-ttu-id="10193-110">Controlar el recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="10193-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="10193-111">Implementar objetos de subprocesamiento controlado.</span><span class="sxs-lookup"><span data-stu-id="10193-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="10193-112">Si bien todos los objetos MAPI se consideran basada en COM porque implementan las interfaces que heredan de [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx), MAPI se desvía en algunas situaciones de las reglas de COM estándar.</span><span class="sxs-lookup"><span data-stu-id="10193-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="10193-113">Este desviación permite a los programadores más flexibilidad en sus implementaciones.</span><span class="sxs-lookup"><span data-stu-id="10193-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="10193-114">Por ejemplo, una interfaz de MAPI, al igual que cualquier interfaz COM, describe un contrato entre implementador y autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="10193-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="10193-115">Una vez que la interfaz se ha creado y publicada, su definición no se puede y no cambia.</span><span class="sxs-lookup"><span data-stu-id="10193-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="10193-116">MAPI no se desvían de esta descripción, pero algo modera la descripción.</span><span class="sxs-lookup"><span data-stu-id="10193-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="10193-117">Los implementadores pueden optar por no implementar métodos concretos, devolver uno de los siguientes valores de error al autor de la llamada:</span><span class="sxs-lookup"><span data-stu-id="10193-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="10193-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="10193-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="10193-119">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="10193-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="10193-120">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="10193-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="10193-121">MAPI_E_TYPE_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="10193-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="10193-122">Las otras desviaciones de las reglas de COM estándar se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="10193-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="10193-123">**Regla de programación de COM**</span><span class="sxs-lookup"><span data-stu-id="10193-123">**COM programming rule**</span></span>|<span data-ttu-id="10193-124">**Variante de MAPI**</span><span class="sxs-lookup"><span data-stu-id="10193-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="10193-125">Todos los parámetros de cadena de los métodos de interfaz deben ser Unicode.</span><span class="sxs-lookup"><span data-stu-id="10193-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="10193-126">Interfaces MAPI se definen para permitir que los parámetros de cadena Unicode o ANSI.</span><span class="sxs-lookup"><span data-stu-id="10193-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="10193-127">Muchos de los métodos que tienen un parámetro de cadena también tienen un parámetro **ulFlags** ; el ancho de un parámetro de cadena se indica mediante el valor de la marca MAPI_UNICODE en **ulFlags**.</span><span class="sxs-lookup"><span data-stu-id="10193-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="10193-128">Algunas interfaces MAPI no admite Unicode y devolver MAPI_E_BAD_CHARWIDTH cuando se establece el indicador MAPI_UNICODE..</span><span class="sxs-lookup"><span data-stu-id="10193-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="10193-129">Todos los métodos de interfaz deben tener un tipo de valor devuelto de HRESULT.</span><span class="sxs-lookup"><span data-stu-id="10193-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="10193-130">MAPI tiene al menos un método que devuelve un valor HRESULT que no sean: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="10193-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="10193-131">Los autores de llamadas y los implementadores deben asignar y liberar memoria para los parámetros de la interfaz mediante la asignadores de tarea COM estándares.</span><span class="sxs-lookup"><span data-stu-id="10193-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="10193-132">Todos los métodos MAPI utilizan la asignadores vinculados [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md) para administrar la memoria para los parámetros de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="10193-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="10193-133">Todas las implementaciones de MAPI de interfaces definidas por OLE, como [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx), use la asignadores de tarea COM estándares.</span><span class="sxs-lookup"><span data-stu-id="10193-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="10193-134">Cerrar todos los parámetros de puntero explícitamente se deben establecer en NULL cuando se produce un error en un método.</span><span class="sxs-lookup"><span data-stu-id="10193-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="10193-135">Interfaces MAPI requieren que los parámetros de puntero estar establecido en NULL o no se modifican cuando un método de salida se produce un error.</span><span class="sxs-lookup"><span data-stu-id="10193-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="10193-136">Todas las implementaciones de MAPI de interfaces definidas por OLE establecer explícitamente los parámetros en NULL en caso de error de salida.</span><span class="sxs-lookup"><span data-stu-id="10193-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="10193-137">Implementar objetos agregables siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="10193-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="10193-138">Interfaces MAPI no están agregables.</span><span class="sxs-lookup"><span data-stu-id="10193-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="10193-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="10193-139">See also</span></span>



[<span data-ttu-id="10193-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="10193-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="10193-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="10193-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="10193-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="10193-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="10193-143">Objeto MAPI e Introducción a la interfaz</span><span class="sxs-lookup"><span data-stu-id="10193-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

