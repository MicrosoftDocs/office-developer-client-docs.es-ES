---
title: Gender
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7abc62938b3c33e42adedfe8ccd66e072314e333
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816908"
---
# <a name="gender"></a>Gender

  
  
**Hace referencia a**: Outlook 
  
Especifica los valores posibles para el género de un usuario de mensajería.
  
## <a name="quick-info"></a>Información rápida

```cpp
enum Gender { 
    genderMin = 0, 
    genderUnspecified = genderMin, 
    genderFemale, 
    genderMale, 
    genderCount, 
    genderMax = genderCount - 1 
}; 

```

## <a name="members"></a>Members

 _genderMin_
  
> El número mínimo de diferentes valores admitidos para el género.
    
 _genderUnspecified_
  
> No se especifica el género para el usuario de mensajería.
    
 _genderFemale_
  
> El usuario de mensajería es femenino.
    
 _genderMale_
  
> El usuario de mensajería es masculino.
    
 _genderCount_
  
> El número de valores diferentes compatibles para el género.
    
 _genderMax_
  
> El número máximo de diferentes valores admitidos para el género.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagGender](pidtaggender-canonical-property.md)

