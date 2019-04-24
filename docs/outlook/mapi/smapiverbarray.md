---
title: SMAPIVerbArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerbArray
api_type:
- COM
ms.assetid: 8736f75c-3e95-42dd-9bc1-2f0bd23c4a02
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7cba5dce60ce15ddb12776d619143849298aac9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357480"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de estructuras [SMAPIVerb](smapiverb.md) que describen los verbos de MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm. h  <br/> |
|Macro relacionada:  <br/> |[CbMAPIVerbArray](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a>Members

 **cForms**
  
> Número de verbos de la matriz.
    
 **aFormInfo**
  
> Matriz de verbos MAPI.
    
## <a name="remarks"></a>Comentarios

La estructura **SMAPIVerbArray** se pasa como un parámetro en el método [IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md) . 
  
## <a name="see-also"></a>Vea también



[SMAPIVerb](smapiverb.md)


[Estructuras MAPI](mapi-structures.md)

