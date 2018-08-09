---
title: IOlkApptRebaserBeginRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed50422e-9edf-4b73-1789-340b70532621
description: Comienza una tarea para cita reajustar una lista de citas, suele obtenida a partir de IOlkApptRebaser::EndEnumerateAppointments.
ms.openlocfilehash: 2becb305eebe448e2adecf91c2a111f86d97fe50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816258"
---
# <a name="iolkapptrebaserbeginrebaseappointments"></a>IOlkApptRebaser::BeginRebaseAppointments

Comienza una tarea para cita reajustar una lista de citas, suele obtenida a partir de [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).
  
## <a name="quick-info"></a>Información rápida

Consulte [IOlkApptRebaser](iolkapptrebaser.md).
  
```cpp
HRESULT BeginRebaseAppointments( 
    const SRowSet *pRows, 
    PFNREBASETASKPROGRESS pfnProgress, 
    PFNREBASETASKCOMPLETE pfnComplete, 
    void **ppContext);
```

## <a name="parameters"></a>Sintaxis

_pRows_
  
> [in] Requerido. Puntero a una estructura [SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) que describe las citas que necesitan el reajuste. Esta estructura suele obtenerse a partir de una llamada anterior a [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).
    
_pfnProgress_
  
> [in] Opcional. Un puntero a una función de progreso de tarea de reajuste para recibir el curso. **PFNREBASETASKPROGRESS** se define en tzmovelib.h. 
    
_pfnComplete_
  
> [out] Opcional. Un puntero a una función de finalización de tarea de reajuste para recibir la notificación de finalización de reajuste. **PFNREBASETASKCOMPLETE** se define en tzmovelib.h. 
    
_ppContext_
  
> [out] Requerido. Puntero a un puntero al contexto devuelto. Este contexto se pasan generalmente a [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Notas

Esta tarea se ejecuta en un subproceso nuevo.
  
## <a name="see-also"></a>Vea también

- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

