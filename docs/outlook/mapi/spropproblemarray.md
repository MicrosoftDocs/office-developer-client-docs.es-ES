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
ms.openlocfilehash: f78e0ed939e190a9855ea4b040d18c01cfecc91d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406860"
---
# <a name="spropproblemarray"></a>SPropProblemArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de una o varias [estructuras SPropProblem.](spropproblem.md) 
  
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
  
> Recuento de [estructuras SPropProblem](spropproblem.md) en la matriz indicada por el **miembro aProblem.** 
    
 **aProblem**
  
> Matriz de **estructuras SPropProblem,** cada una que describe un error de propiedad. 
    
## <a name="remarks"></a>Comentarios

Para obtener más información acerca de cómo funcionan las estructuras **SPropProblem** y **SPropProblemArray** con errores relacionados con las propiedades, vea [Mapi Named Properties](mapi-named-properties.md). 
  
## <a name="see-also"></a>Vea también



[SCODE](scode.md)
  
[SPropProblem](spropproblem.md)


[Estructuras MAPI](mapi-structures.md)

