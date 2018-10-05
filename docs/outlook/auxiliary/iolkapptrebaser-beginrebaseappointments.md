---
title: IOlkApptRebaserBeginRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed50422e-9edf-4b73-1789-340b70532621
description: Comienza una tarea para cita reajustar una lista de citas, suele obtenida a partir de IOlkApptRebaser::EndEnumerateAppointments.
ms.openlocfilehash: f0f2377f30de7688aaa4196e3a046c664c2128aa
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396095"
---
# <a name="iolkapptrebaserbeginrebaseappointments"></a><span data-ttu-id="4edf1-103">IOlkApptRebaser::BeginRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="4edf1-103">IOlkApptRebaser::BeginRebaseAppointments</span></span>

<span data-ttu-id="4edf1-104">Comienza una tarea para cita reajustar una lista de citas, suele obtenida a partir de [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="4edf1-104">Begins a task for appointment rebasing given a list of appointments, usually obtained from [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4edf1-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="4edf1-105">Quick info</span></span>

<span data-ttu-id="4edf1-106">Consulte [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="4edf1-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT BeginRebaseAppointments( 
    const SRowSet *pRows, 
    PFNREBASETASKPROGRESS pfnProgress, 
    PFNREBASETASKCOMPLETE pfnComplete, 
    void **ppContext);
```

## <a name="parameters"></a><span data-ttu-id="4edf1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4edf1-107">Parameters</span></span>

<span data-ttu-id="4edf1-108">_pRows_</span><span class="sxs-lookup"><span data-stu-id="4edf1-108">_pRows_</span></span>
  
> <span data-ttu-id="4edf1-p101">[in] Requerido. Puntero a una estructura [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) que describe las citas que necesitan el reajuste. Esta estructura suele obtenerse a partir de una llamada anterior a [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="4edf1-p101">[in] Required. A pointer to an [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing. This structure is usually obtained from a prior call to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
    
<span data-ttu-id="4edf1-112">_pfnProgress_</span><span class="sxs-lookup"><span data-stu-id="4edf1-112">_pfnProgress_</span></span>
  
> <span data-ttu-id="4edf1-p102">[in] Opcional. Un puntero a una función de progreso de tarea de reajuste para recibir el curso. **PFNREBASETASKPROGRESS** se define en tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="4edf1-p102">[in] Optional. A pointer to a rebase task progress function to receive progress. **PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="4edf1-116">_pfnComplete_</span><span class="sxs-lookup"><span data-stu-id="4edf1-116">_pfnComplete_</span></span>
  
> <span data-ttu-id="4edf1-p103">[out] Opcional. Un puntero a una función de finalización de tarea de reajuste para recibir la notificación de finalización de reajuste. **PFNREBASETASKCOMPLETE** se define en tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="4edf1-p103">[out] Optional. A pointer to a rebase task completion function to receive notification of rebase completion. **PFNREBASETASKCOMPLETE** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="4edf1-120">_ppContext_</span><span class="sxs-lookup"><span data-stu-id="4edf1-120">_ppContext_</span></span>
  
> <span data-ttu-id="4edf1-p104">[out] Requerido. Puntero a un puntero al contexto devuelto. Este contexto se pasan generalmente a [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="4edf1-p104">[out] Required. A pointer to a pointer to the returned context. This context will usually be passed to [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="4edf1-124">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="4edf1-124">Return values</span></span>

<span data-ttu-id="4edf1-125">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="4edf1-125">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4edf1-126">Notas</span><span class="sxs-lookup"><span data-stu-id="4edf1-126">Remarks</span></span>

<span data-ttu-id="4edf1-127">Esta tarea se ejecuta en un subproceso nuevo.</span><span class="sxs-lookup"><span data-stu-id="4edf1-127">This task runs on a new thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4edf1-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4edf1-128">See also</span></span>

- [<span data-ttu-id="4edf1-129">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="4edf1-129">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

