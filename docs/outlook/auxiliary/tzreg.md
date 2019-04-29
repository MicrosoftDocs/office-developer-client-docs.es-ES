---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Define cuándo se inicia el horario de verano, Cuándo se produce el cambio de hora estándar y cuántas horas tiene el horario de verano.
ms.openlocfilehash: 136ff6ad0c1a9bc2ad61ef7ba698d66d645165d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419369"
---
# <a name="tzreg"></a>TZREG

Define cuándo se inicia el horario de verano, Cuándo se produce el cambio de hora estándar y cuántas horas tiene el horario de verano.
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a>Miembros

_lBias_
  
> El desplazamiento de la hora media de Greenwich (GMT).
    
_lStandardBias_
  
> Desplazamiento respecto a la inclinación en el horario estándar.
    
_lDaylightBias_
  
> Desplazamiento respecto a bias durante el horario de verano.
    
_stStandardDate_
  
> Hora a la que se va a cambiar a la hora estándar.
    
_stDaylightDate_
  
> Hora para cambiar al horario de verano.
    
## <a name="remarks"></a>Comentarios

Esta estructura es similar a **TIME_ZONE_INFORMATION**. Esta es la estructura que usan los clientes heredados para almacenar la información de zona horaria de las reuniones periódicas.
  
## <a name="see-also"></a>Ver también

- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)

