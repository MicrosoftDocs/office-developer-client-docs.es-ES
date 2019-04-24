---
title: SizedSPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropProblemArray
api_type:
- COM
ms.assetid: 2fc3febb-8c69-4315-a112-a28eee98013d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b3818e5e1429c7e2b7d5f7533db733ba29e672c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282694"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura [SPropProblemArray](spropproblemarray.md) con nombre que contiene un número especificado de estructuras [SPropProblem](spropproblem.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Estructura relacionada:  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>Parameters

__cprob_
  
> Número de estructuras **SPropProblem** que se incluirán en la nueva estructura. 
    
__nombre_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

Use la macro **SizedSPropProblemArray** para crear una matriz con problemas de propiedad con límites explícitos. Para usar la nueva estructura que resulta de la macro **SizedSPropProblemArray** como un puntero a una estructura **SPropProblemArray** , realice la siguiente conversión: 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>Vea también

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

