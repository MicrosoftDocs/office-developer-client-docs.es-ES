---
title: IOlkApptRebaserEndRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e47d5a8d-6a13-f430-fbfd-00df04b4a006
description: Espera a que cita el reajuste para completar y recupera los resultados.
ms.openlocfilehash: a6e62cff9efea1fc7079d04bc9b032b5637f8847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321892"
---
# <a name="iolkapptrebaserendrebaseappointments"></a><span data-ttu-id="befed-103">IOlkApptRebaser::EndRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="befed-103">IOlkApptRebaser::EndRebaseAppointments</span></span>

<span data-ttu-id="befed-104">Espera a que cita el reajuste para completar y recupera los resultados.</span><span class="sxs-lookup"><span data-stu-id="befed-104">Waits for appointment rebasing to complete and retrieves the results.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="befed-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="befed-105">Quick info</span></span>

<span data-ttu-id="befed-106">Consulte [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="befed-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT EndRebaseAppointments( 
    void *pContext, 
    HRESULT *phResult);
```

## <a name="parameters"></a><span data-ttu-id="befed-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="befed-107">Parameters</span></span>

<span data-ttu-id="befed-108">_pContext_</span><span class="sxs-lookup"><span data-stu-id="befed-108">_pContext_</span></span>
  
> <span data-ttu-id="befed-p101">[in] Requerido. Un puntero al contexto que se obtiene de una llamada a [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="befed-p101">[in] Required. A pointer to the context obtained from a call to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="befed-111">_phResult_</span><span class="sxs-lookup"><span data-stu-id="befed-111">_phResult_</span></span>
  
> <span data-ttu-id="befed-p102">[out] Requerido. Puntero a un **valor HRESULT** para recuperar el resultado de la operación de reajuste.</span><span class="sxs-lookup"><span data-stu-id="befed-p102">[out] Required. A pointer to an **HRESULT** to retrieve the result of the rebasing operation.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="befed-114">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="befed-114">Return values</span></span>

<span data-ttu-id="befed-115">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="befed-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="befed-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="befed-116">See also</span></span>

- [<span data-ttu-id="befed-117">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="befed-117">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

