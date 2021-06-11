---
title: IOlkApptRebaserBeginEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8946703a-aaa8-6b3f-aa68-931365db620d
description: Se inicia una tarea de enumeración de la cita en una carpeta de calendario para buscar las citas que necesitan el reajuste.
ms.openlocfilehash: cc89b3510f09bb98fd6720cb6d5ab3edeb13eac8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407273"
---
# <a name="iolkapptrebaserbeginenumerateappointments"></a>IOlkApptRebaser::BeginEnumerateAppointments

Se inicia una tarea de enumeración de la cita en una carpeta de calendario para buscar las citas que necesitan el reajuste.
  
## <a name="quick-info"></a>Información rápida

Consulte [IOlkApptRebaser](iolkapptrebaser.md).
  
```cpp
HRESULT BeginEnumerateAppointments( 
    PFNREBASETASKPROGRESS pfnProgress, 
    void **ppContext);
```

## <a name="parameters"></a>Parameters

_pfnProgress_
  
> [in] Opcional. Un puntero a una función de progreso de tarea de reajuste para recibir el curso. **PFNREBASETASKPROGRESS** se define en tzmovelib.h. 
    
_ppContext_
  
> [out] Requerido. Puntero a un puntero al contexto devuelto. Este contexto se pasará a [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Comentarios

Esta tarea se ejecuta en un subproceso nuevo.
  
## <a name="see-also"></a>Vea también

- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

