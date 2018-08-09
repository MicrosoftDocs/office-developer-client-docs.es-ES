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
ms.openlocfilehash: 1767c86cb5390572b95530060f2295034ed35f43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820726"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**Hace referencia a**: Outlook 
  
Contiene una matriz de estructuras [SMAPIVerb](smapiverb.md) que describen los verbos de MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm.h  <br/> |
|Macro relacionado:  <br/> |[CbMAPIVerbArray](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a>Members

 **cForms**
  
> Recuento de verbos en la matriz.
    
 **aFormInfo**
  
> Matriz de los verbos de MAPI.
    
## <a name="remarks"></a>Comentarios

La estructura **SMAPIVerbArray** se pasa como un parámetro en el método [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) . 
  
## <a name="see-also"></a>Vea también



[SMAPIVerb](smapiverb.md)


[Estructuras MAPI](mapi-structures.md)

