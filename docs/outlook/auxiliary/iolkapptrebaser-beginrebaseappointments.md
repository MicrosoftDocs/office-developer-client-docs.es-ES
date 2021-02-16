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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321913"
---
# <a name="iolkapptrebaserbeginrebaseappointments"></a><span data-ttu-id="0017e-103">IOlkApptRebaser::BeginRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="0017e-103">IOlkApptRebaser::BeginRebaseAppointments</span></span>

<span data-ttu-id="0017e-104">Comienza una tarea para cita reajustar una lista de citas, suele obtenida a partir de [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="0017e-104">Begins a task for appointment rebasing given a list of appointments, usually obtained from [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0017e-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="0017e-105">Quick info</span></span>

<span data-ttu-id="0017e-106">Consulte [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="0017e-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT BeginRebaseAppointments( 
    const SRowSet *pRows, 
    PFNREBASETASKPROGRESS pfnProgress, 
    PFNREBASETASKCOMPLETE pfnComplete, 
    void **ppContext);
```

## <a name="parameters"></a><span data-ttu-id="0017e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0017e-107">Parameters</span></span>

<span data-ttu-id="0017e-108">_pRows_</span><span class="sxs-lookup"><span data-stu-id="0017e-108">_pRows_</span></span>
  
> <span data-ttu-id="0017e-p101">[in] Requerido. Puntero a una estructura [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) que describe las citas que necesitan el reajuste. Esta estructura suele obtenerse a partir de una llamada anterior a [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="0017e-p101">[in] Required. A pointer to an [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing. This structure is usually obtained from a prior call to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
    
<span data-ttu-id="0017e-112">_pfnProgress_</span><span class="sxs-lookup"><span data-stu-id="0017e-112">_pfnProgress_</span></span>
  
> <span data-ttu-id="0017e-p102">[in] Opcional. Un puntero a una función de progreso de tarea de reajuste para recibir el curso. **PFNREBASETASKPROGRESS** se define en tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="0017e-p102">[in] Optional. A pointer to a rebase task progress function to receive progress. **PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="0017e-116">_pfnComplete_</span><span class="sxs-lookup"><span data-stu-id="0017e-116">_pfnComplete_</span></span>
  
> <span data-ttu-id="0017e-p103">[out] Opcional. Un puntero a una función de finalización de tarea de reajuste para recibir la notificación de finalización de reajuste. **PFNREBASETASKCOMPLETE** se define en tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="0017e-p103">[out] Optional. A pointer to a rebase task completion function to receive notification of rebase completion. **PFNREBASETASKCOMPLETE** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="0017e-120">_ppContext_</span><span class="sxs-lookup"><span data-stu-id="0017e-120">_ppContext_</span></span>
  
> <span data-ttu-id="0017e-p104">[out] Requerido. Puntero a un puntero al contexto devuelto. Este contexto se pasan generalmente a [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="0017e-p104">[out] Required. A pointer to a pointer to the returned context. This context will usually be passed to [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="0017e-124">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="0017e-124">Return values</span></span>

<span data-ttu-id="0017e-125">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="0017e-125">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0017e-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0017e-126">Remarks</span></span>

<span data-ttu-id="0017e-127">Esta tarea se ejecuta en un subproceso nuevo.</span><span class="sxs-lookup"><span data-stu-id="0017e-127">This task runs on a new thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0017e-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0017e-128">See also</span></span>

- [<span data-ttu-id="0017e-129">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="0017e-129">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

