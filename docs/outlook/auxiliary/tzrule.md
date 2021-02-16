---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Especifica información para una regla de zona horaria sobre cuándo se inicia el horario de verano y el año en que esa regla de zona horaria primero surte efecto.
ms.openlocfilehash: 71ede7c0061a058c2dd85c7b9b36c42583a6bb84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328619"
---
# <a name="tzrule"></a>TZRULE

Especifica información para una regla de zona horaria sobre cuándo se inicia el horario de verano y el año en que esa regla de zona horaria primero surte efecto. 
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a>Miembros

_wFlags_
  
> Las marcas establecidas para este miembro identifican detalles específicos para esta regla de zona horaria. Las marcas posibles son las siguientes:
    
   - **TZRULE_FLAG_EFFECTIVE_TZREG:** identifica la regla como la que debe usarse actualmente. Solo se puede marcar una regla como la regla efectiva. Todas las demás reglas son solo para fines de comparación. 
    
   - **TZRULE_FLAG_RECUR_CURRENT_TZREG:** en reuniones periódicas, identifica la regla como que coincide con la regla en [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx). Esto se puede usar para detectar si un cliente heredado ha modificado significativamente **PidLidTimeZoneStruct,** lo que de lo contrario no sería consciente de la nueva propiedad más completa. 
    
_stStart_
  
> La hora en hora universal coordinada (UTC) que inició la regla de zona horaria.
    
_TZReg_
  
> La información de zona horaria de la regla de zona horaria.
    
## <a name="remarks"></a>Comentarios

Esta estructura aumenta [TZREG](tzreg.md) proporcionando información adicional que indica cuándo surte efecto la regla de zona horaria. 
  
## <a name="see-also"></a>Consulte también

- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [Constantes (API exportadas de Outlook)](constants-outlook-exported-apis.md)
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
- [TZDEFINITION](tzdefinition.md)

