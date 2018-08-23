---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7622baaebf6918cf84c48e53291cf5ec2c0b1a4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572567"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura de [SSortOrderSet](ssortorderset.md) con nombre que contiene un número especificado de criterios de ordenación. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |**SSortOrderSet** <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a>Parámetros

__csort_
  
> Recuento de criterios de ordenación que se deben incluir en la nueva estructura.
    
__nombre_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

Use la macro **SizedSSortOrderSet** para crear un criterio de ordenación establecer con límites explícitos. 
  
Para usar la nueva estructura que el resultado de la macro **SizedSSortOrderSet** como un puntero a una estructura **SSortOrderSet** , realice la conversión de tipos siguiente: 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a>Recursos adicionales

- [SSortOrderSet](ssortorderset.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

