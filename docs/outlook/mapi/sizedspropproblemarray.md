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
ms.openlocfilehash: b8521172b441bd26a6562aa28f836d453544928f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820681"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**Hace referencia a**: Outlook 
  
Crea una estructura de [SPropProblemArray](spropproblemarray.md) con nombre que contiene un número especificado de estructuras [SPropProblem](spropproblem.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>Parámetros

__cprob_
  
> Recuento de las estructuras de **SPropProblem** que se deben incluir en la nueva estructura. 
    
__nombre_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

Use la macro **SizedSPropProblemArray** para crear una matriz de propiedad problema con límites explícitos. Para usar la nueva estructura que el resultado de la macro **SizedSPropProblemArray** como un puntero a una estructura **SPropProblemArray** , realice la conversión de tipos siguiente: 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>Vea también

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

