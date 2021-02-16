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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418116"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura [SPropProblemArray con](spropproblemarray.md) nombre que contiene un número especificado de [estructuras SPropProblem.](spropproblem.md) 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionada:  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>Parámetros

_ _cprob_
  
> Número de **estructuras SPropProblem** que se incluirán en la nueva estructura. 
    
_ _name_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

Use la macro **SizedSPropProblemArray** para crear una matriz de problemas de propiedad con límites explícitos. Para usar la nueva estructura que resulta de la macro **SizedSPropProblemArray** como puntero a una estructura **SPropProblemArray,** realice la conversión siguiente: 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>Consulte también

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

