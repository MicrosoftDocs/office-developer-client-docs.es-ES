---
title: SPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblemArray
api_type:
- COM
ms.assetid: 3fbaa77a-be43-4fce-af67-1826ee101799
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e71658922b6cb80dadc7e034a51c10189c4207ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568500"
---
# <a name="spropproblemarray"></a>SPropProblemArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de uno o más estructuras [SPropProblem](spropproblem.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macros relacionadas:  <br/> |[CbNewSPropProblemArray](cbnewspropproblemarray.md) <br/> [CbSPropProblemArray](cbspropproblemarray.md) <br/> [SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a>Members

 **cProblem**
  
> Recuento de las estructuras de [SPropProblem](spropproblem.md) en la matriz indicada por el miembro **aProblem** . 
    
 **aProblem**
  
> Matriz de estructuras **SPropProblem** , que describe un error de propiedad. 
    
## <a name="remarks"></a>Comentarios

Para obtener más información acerca de cómo funcionan las estructuras **SPropProblem** y **SPropProblemArray** con errores relacionados con las propiedades, vea [Propiedades de nombre de MAPI](mapi-named-properties.md). 
  
## <a name="see-also"></a>Recursos adicionales



[SCODE](scode.md)
  
[SPropProblem](spropproblem.md)


[Estructuras MAPI](mapi-structures.md)

