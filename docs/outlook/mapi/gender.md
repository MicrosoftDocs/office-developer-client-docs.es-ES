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
ms.openlocfilehash: 042216df309e98f35ed0ad71742e46300ebb06da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428651"
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

## <a name="members"></a>Miembros

 _genderMin_
  
> El número mínimo de valores diferentes admitidos para el sexo.
    
 _genderUnspecified_
  
> No se ha especificado el sexo del usuario de mensajería.
    
 _genderFemale_
  
> El usuario de mensajería es hembra.
    
 _genderMale_
  
> El usuario de mensajería es macho.
    
 _genderCount_
  
> El número de valores diferentes admitidos para el género.
    
 _genderMax_
  
> El número máximo de valores diferentes admitidos para el sexo.
    
## <a name="see-also"></a>Ver también



[Propiedad canónica PidTagGender](pidtaggender-canonical-property.md)

