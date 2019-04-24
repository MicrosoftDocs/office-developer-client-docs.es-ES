---
title: IOlkApptRebaserEndEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc4506c7-7a4f-940d-d0a6-e0fab4561a88
description: Espera de enumeración de la cita en una carpeta de calendario para completar y devuelve una lista de citas esa necesidad de reajuste.
ms.openlocfilehash: 5be6fd9ce33374725b36429cd0fbc717776c9ab9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321906"
---
# <a name="iolkapptrebaserendenumerateappointments"></a><span data-ttu-id="d041e-103">IOlkApptRebaser::EndEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="d041e-103">IOlkApptRebaser::EndEnumerateAppointments</span></span>

<span data-ttu-id="d041e-104">Espera de enumeración de la cita en una carpeta de calendario para completar y devuelve una lista de citas esa necesidad de reajuste.</span><span class="sxs-lookup"><span data-stu-id="d041e-104">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d041e-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="d041e-105">Quick info</span></span>

<span data-ttu-id="d041e-106">Consulte [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="d041e-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT EndEnumerateAppointments( 
    void *pContext, 
    HRESULT *phResult, 
    MAPIERROR **ppError, 
    SRowSet **ppRows);
```

## <a name="parameters"></a><span data-ttu-id="d041e-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="d041e-107">Parameters</span></span>

<span data-ttu-id="d041e-108">_pContext_</span><span class="sxs-lookup"><span data-stu-id="d041e-108">_pContext_</span></span>
  
> <span data-ttu-id="d041e-p101">[in] Requerido. Un puntero al contexto obtenido de una llamada anterior a [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="d041e-p101">[in] Required. A pointer to the context obtained from a prior call to [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md).</span></span>
    
<span data-ttu-id="d041e-111">_phResult_</span><span class="sxs-lookup"><span data-stu-id="d041e-111">_phResult_</span></span>
  
> <span data-ttu-id="d041e-p102">[out] Requerido. Puntero a un **valor HRESULT** para recuperar los resultados de la operación de enumeración.</span><span class="sxs-lookup"><span data-stu-id="d041e-p102">[out] Required. A pointer to an **HRESULT** to retrieve the results of the enumeration operation.</span></span> 
    
<span data-ttu-id="d041e-114">_ppError_</span><span class="sxs-lookup"><span data-stu-id="d041e-114">_ppError_</span></span>
  
> <span data-ttu-id="d041e-p103">[out] Opcional. Un puntero a un puntero a una estructura **MAPIERROR** para recuperar información de error extendida.</span><span class="sxs-lookup"><span data-stu-id="d041e-p103">[out] Optional. A pointer to a pointer to a **MAPIERROR** structure to retrieve extended error information.</span></span> 
    
<span data-ttu-id="d041e-117">_ppRows_</span><span class="sxs-lookup"><span data-stu-id="d041e-117">_ppRows_</span></span>
  
> <span data-ttu-id="d041e-p104">[out] Requerido. Un puntero a un puntero a una estructura [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) que describe las citas que necesitan el reajuste. Esta estructura se pasan generalmente a [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="d041e-p104">[out] Required. A pointer to a pointer to an [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing. This structure will usually be passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="d041e-121">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="d041e-121">Return values</span></span>

<span data-ttu-id="d041e-122">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="d041e-122">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d041e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d041e-123">See also</span></span>

- [<span data-ttu-id="d041e-124">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="d041e-124">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

