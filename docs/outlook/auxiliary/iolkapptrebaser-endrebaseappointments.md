---
title: IOlkApptRebaserEndRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e47d5a8d-6a13-f430-fbfd-00df04b4a006
description: Espera a que cita el reajuste para completar y recupera los resultados.
ms.openlocfilehash: fd27021ce05b1d5b95fd258e0ee89b5bd4f2c7db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816254"
---
# <a name="iolkapptrebaserendrebaseappointments"></a>IOlkApptRebaser::EndRebaseAppointments

Espera a que cita el reajuste para completar y recupera los resultados.
  
## <a name="quick-info"></a>Información rápida

Consulte [IOlkApptRebaser](iolkapptrebaser.md).
  
```cpp
HRESULT EndRebaseAppointments( 
    void *pContext, 
    HRESULT *phResult);
```

## <a name="parameters"></a>Sintaxis

_pContext_
  
> [in] Requerido. Un puntero al contexto que se obtiene de una llamada a [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).
    
_phResult_
  
> [out] Requerido. Puntero a un **valor HRESULT** para recuperar el resultado de la operación de reajuste. 
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="see-also"></a>Vea también

- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

