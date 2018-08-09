---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Representa una zona horaria toda incluidas todas las reglas de MAYÚS históricas, actuales y futuros zona horaria para el horario de verano.
ms.openlocfilehash: f436216f5da882ea8ac144e6bd384e51e31abb8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816358"
---
# <a name="tzdefinition"></a>TZDEFINITION

Representa una zona horaria toda incluidas todas las reglas de MAYÚS históricas, actuales y futuros zona horaria para el horario de verano.
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a>Members

_wFlags_
  
> Indica que el nombre de la clave que representa la zona horaria en el registro de Windows es válido. Debido a que cada zona horaria siempre debe identificarse mediante un nombre de clave, este miembro siempre debe tener el valor **TZDEFINITION_FLAG_VALID_KEYNAME**.
    
_pwszKeyName_
  
> El nombre de la clave de esta zona horaria en el registro de Windows. Este nombre no debe localizarse. Tiene un tamaño máximo de **MAX_PATH**, que se define en el windows.h de archivo de encabezado de Kit de desarrollo de Software (SDK) de Windows. 
    
_cRules_
  
> El número de reglas de zona horaria para esta definición. El número máximo de reglas es **TZ_MAX_RULES**. 
    
_rgRules_
  
> Una matriz de reglas que describen cuando se producen cambios.
    
## <a name="remarks"></a>Comentarios

Debe haber al menos una regla en *rgRules* . La primera regla en *rgRules* es considerado como la regla para utilizar hasta que se inicia la segunda regla, independientemente de la *stStart* en la primera regla. 
  
Las reglas se deben ordenar de más antiguo a más reciente. No hay ninguna superposición permitida entre las reglas, por lo que se considera una regla anterior para finalizar cuando se inicia una nueva regla.
  
## <a name="see-also"></a>Vea también

- [Constantes (API exportadas de Outlook)](constants-outlook-exported-apis.md)
- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)

