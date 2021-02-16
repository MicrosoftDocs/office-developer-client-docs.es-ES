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

## <a name="parameters"></a>Parámetros

_pRows_
  
> [in] Requerido. Puntero a una estructura [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) que describe las citas que necesitan el reajuste. Esta estructura suele obtenerse a partir de una llamada anterior a [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).
    
_pfnProgress_
  
> [in] Opcional. Un puntero a una función de progreso de tarea de reajuste para recibir el curso. **PFNREBASETASKPROGRESS** se define en tzmovelib.h. 
    
_pfnComplete_
  
> [out] Opcional. Un puntero a una función de finalización de tarea de reajuste para recibir la notificación de finalización de reajuste. **PFNREBASETASKCOMPLETE** se define en tzmovelib.h. 
    
_ppContext_
  
> [out] Requerido. Puntero a un puntero al contexto devuelto. Este contexto se pasan generalmente a [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Comentarios

Esta tarea se ejecuta en un subproceso nuevo.
  
## <a name="see-also"></a>Consulte también

- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

