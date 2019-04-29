---
title: IsEqualMAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IsEqualMAPIUID
api_type:
- COM
ms.assetid: 85d71b73-0630-4c5d-b0e3-b48d27a300d0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 44e3613338c8932bc80dd1150392033dfa3cd050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426936"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Prueba dos estructuras [MAPIUID](mapiuid.md) para determinar si contienen el mismo identificador. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Estructura relacionada:  <br/> |**MAPIUID** <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a>Parameters

 _lpuid1_
  
> Puntero a la primera estructura **MAPIUID** que se va a probar. 
    
 _lpuid2_
  
> Puntero a la segunda estructura **MAPIUID** que se va a probar. 
    
## <a name="remarks"></a>Comentarios

La macro **IsEqualMAPIUID** devuelve true si las dos estructuras **MAPIUID** contienen el mismo identificador y false en caso contrario. 
  
La macro **IsEqualMAPIUID** requiere que se incluya el archivo de encabezado Memory. h. 
  
## <a name="see-also"></a>Ver también



[MAPIUID](mapiuid.md)


[Macros relacionadas con estructuras](macros-related-to-structures.md)

