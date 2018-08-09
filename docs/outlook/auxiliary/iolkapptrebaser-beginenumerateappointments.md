---
title: IOlkApptRebaserBeginEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8946703a-aaa8-6b3f-aa68-931365db620d
description: Se inicia una tarea de enumeración de la cita en una carpeta de calendario para buscar las citas que necesitan el reajuste.
ms.openlocfilehash: 2ad26692483d87166a538ec2f04d3fc13b9ea930
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816239"
---
# <a name="iolkapptrebaserbeginenumerateappointments"></a><span data-ttu-id="b757f-103">IOlkApptRebaser::BeginEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="b757f-103">IOlkApptRebaser::BeginEnumerateAppointments</span></span>

<span data-ttu-id="b757f-104">Se inicia una tarea de enumeración de la cita en una carpeta de calendario para buscar las citas que necesitan el reajuste.</span><span class="sxs-lookup"><span data-stu-id="b757f-104">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b757f-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b757f-105">Quick info</span></span>

<span data-ttu-id="b757f-106">Consulte [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="b757f-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT BeginEnumerateAppointments( 
    PFNREBASETASKPROGRESS pfnProgress, 
    void **ppContext);
```

## <a name="parameters"></a><span data-ttu-id="b757f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b757f-107">Parameters</span></span>

<span data-ttu-id="b757f-108">_pfnProgress_</span><span class="sxs-lookup"><span data-stu-id="b757f-108">_pfnProgress_</span></span>
  
> <span data-ttu-id="b757f-p101">[in] Opcional. Un puntero a una función de progreso de tarea de reajuste para recibir el curso. **PFNREBASETASKPROGRESS** se define en tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="b757f-p101">[in] Optional. A pointer to a rebase task progress function to receive progress. **PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="b757f-112">_ppContext_</span><span class="sxs-lookup"><span data-stu-id="b757f-112">_ppContext_</span></span>
  
> <span data-ttu-id="b757f-p102">[out] Requerido. Puntero a un puntero al contexto devuelto. Este contexto se pasará a [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="b757f-p102">[out] Required. A pointer to a pointer to the returned context. This context will be passed to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="b757f-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="b757f-116">Return values</span></span>

<span data-ttu-id="b757f-117">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="b757f-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b757f-118">Notas</span><span class="sxs-lookup"><span data-stu-id="b757f-118">Remarks</span></span>

<span data-ttu-id="b757f-119">Esta tarea se ejecuta en un subproceso nuevo.</span><span class="sxs-lookup"><span data-stu-id="b757f-119">This task runs on a new thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b757f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="b757f-120">See also</span></span>

- [<span data-ttu-id="b757f-121">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="b757f-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

