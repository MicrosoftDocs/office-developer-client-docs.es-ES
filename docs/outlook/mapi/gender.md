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
ms.openlocfilehash: a74a6639023ae6ffddeabd03970b609e7b7babe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588457"
---
# <a name="gender"></a>Gender

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="see-also"></a>Recursos adicionales



[Propiedad canónica PidTagGender](pidtaggender-canonical-property.md)

