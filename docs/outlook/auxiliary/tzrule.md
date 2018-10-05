---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Especifica la información de una regla de zona horaria acerca de cuándo se inicia el horario de verano y el año en el que dicha regla de zona horaria en primer lugar en vigor.
ms.openlocfilehash: 71ede7c0061a058c2dd85c7b9b36c42583a6bb84
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392700"
---
# <a name="tzrule"></a>TZRULE

Especifica la información de una regla de zona horaria acerca de cuándo se inicia el horario de verano y el año en el que dicha regla de zona horaria en primer lugar en vigor. 
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a>Members

_wFlags_
  
> Los indicadores establecidos para este miembro identifican detalles específicos para esta regla de zona horaria. Los indicadores posibles son los siguientes:
    
   - **TZRULE_FLAG_EFFECTIVE_TZREG** : identifica la regla que el que se debe usar actualmente. Sólo una regla puede estar marcada como la regla eficaz. Todas las demás reglas son únicamente con fines de comparación. 
    
   - **TZRULE_FLAG_RECUR_CURRENT_TZREG** : en las reuniones periódicas, identifica la regla como que coincidan con la regla en [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx). Esto puede usarse para detectar si se ha modificado considerablemente **PidLidTimeZoneStruct** por un cliente heredado, lo que sería en caso contrario, sin ser conscientes de la propiedad nuevo, más completa. 
    
_stStart_
  
> El tiempo en hora Universal coordinada (UTC) que inician la regla de zona horaria.
    
_TZReg_
  
> La información de zona horaria para la regla de zona horaria.
    
## <a name="remarks"></a>Comentarios

Esta estructura aumenta [TZREG](tzreg.md) proporcionando información adicional que indica si las reglas de zona horaria surtan efecto. 
  
## <a name="see-also"></a>Vea también

- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [Constantes (API exportadas de Outlook)](constants-outlook-exported-apis.md)
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
- [TZDEFINITION](tzdefinition.md)

