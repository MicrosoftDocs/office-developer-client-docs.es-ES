---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Define cuándo se inicia el tiempo de horario de verano, cuando se produce la devolución a la hora estándar y es el turno de verano de cuántas horas.
ms.openlocfilehash: 85812ab053d77c07f9360b6bf3a1faaf72cae573
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816348"
---
# <a name="tzreg"></a>TZREG

Define cuándo se inicia el tiempo de horario de verano, cuando se produce la devolución a la hora estándar y es el turno de verano de cuántas horas.
  
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

## <a name="members"></a>Members

_lBias_
  
> El desplazamiento de la hora del meridiano de Greenwich (GMT).
    
_lStandardBias_
  
> Especifica el desplazamiento de inclinación durante el horario estándar.
    
_lDaylightBias_
  
> Especifica el desplazamiento de inclinación durante el horario de verano.
    
_stStandardDate_
  
> El tiempo para cambiar a la hora estándar.
    
_stDaylightDate_
  
> El tiempo para cambiar al horario de verano.
    
## <a name="remarks"></a>Comentarios

Esta estructura es similar a **TIME_ZONE_INFORMATION**. Ésta es la estructura usada por los clientes heredados para almacenar la información de zona horaria de reuniones periódicas.
  
## <a name="see-also"></a>Vea también

- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)

