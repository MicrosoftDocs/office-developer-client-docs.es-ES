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
ms.openlocfilehash: 3fd61828cd631c4abc0131da867ca213a3c44d20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820751"
---
# <a name="spropproblemarray"></a>SPropProblemArray

  
  
**Hace referencia a**: Outlook 
  
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
  
## <a name="see-also"></a>Vea también



[SCODE](scode.md)
  
[SPropProblem](spropproblem.md)


[Estructuras MAPI](mapi-structures.md)

