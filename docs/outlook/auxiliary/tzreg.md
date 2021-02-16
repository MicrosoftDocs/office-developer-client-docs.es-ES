---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Define cuándo se inicia el horario de verano, cuándo se produce la vuelta a la hora estándar y cuántas horas es el turno de verano.
ms.openlocfilehash: 136ff6ad0c1a9bc2ad61ef7ba698d66d645165d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419369"
---
# <a name="tzreg"></a>TZREG

Define cuándo se inicia el horario de verano, cuándo se produce la vuelta al horario estándar y cuántas horas es el turno de verano.
  
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
  
> Desplazamiento de la hora media de Greenwich (GMT).
    
_lStandardBias_
  
> Desplazamiento de la inclinación durante el tiempo estándar.
    
_lDaylightBias_
  
> Desplazamiento de la diferencia durante el horario de verano.
    
_stStandardDate_
  
> Tiempo para cambiar a la hora estándar.
    
_stDaylightDate_
  
> Hora para cambiar al horario de verano.
    
## <a name="remarks"></a>Comentarios

Esta estructura es similar a **TIME_ZONE_INFORMATION**. Esta es la estructura que usan los clientes heredados para almacenar información de zona horaria para reuniones periódicas.
  
## <a name="see-also"></a>Consulte también

- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)

