---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Representa una zona horaria completa, incluidas todas las reglas de cambio de zona horaria históricas, actuales y futuras para el horario de verano.
ms.openlocfilehash: 5f7000ecc1fa602b330670c2ee1c39f673a11a65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429344"
---
# <a name="tzdefinition"></a>TZDEFINITION

Representa una zona horaria completa, incluidas todas las reglas de cambio de zona horaria históricas, actuales y futuras para el horario de verano.
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a>Miembros

_wFlags_
  
> Indica que el nombre de clave que representa la zona horaria en el Windows es válido. Dado que cada zona horaria debe identificarse siempre con un nombre de clave, este miembro siempre debe tener el valor **TZDEFINITION_FLAG_VALID_KEYNAME**.
    
_pwszKeyName_
  
> Nombre de la clave de esta zona horaria en el Windows registro. Este nombre no debe estar localizado. Tiene un tamaño máximo de **MAX_PATH**, que se define en el archivo de encabezado Windows Software Development Kit (SDK) windows.h. 
    
_cRules_
  
> Número de reglas de zona horaria para esta definición. El número máximo de reglas **es TZ_MAX_RULES**. 
    
_rgRules_
  
> Una matriz de reglas que describen cuándo se producen los turnos.
    
## <a name="remarks"></a>Comentarios

Debe haber al menos una regla en  *rgRules*  . La primera regla de  *rgRules*  se considera la regla que se usará hasta que se inicie la segunda regla, independientemente del  *stStart*  de la primera regla. 
  
Las reglas deben ordenarse de la más antigua a la más reciente. No se permite superposición entre reglas, por lo que se considera que una regla anterior finaliza cuando se inicia una nueva regla.
  
## <a name="see-also"></a>Vea también

- [Constantes (API exportadas de Outlook)](constants-outlook-exported-apis.md)
- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)

