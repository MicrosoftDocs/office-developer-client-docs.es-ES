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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 635a4a872b83a2996b1a0198975a0ecd2cd906eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817957"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**Se aplica a**: Outlook 
  
Prueba dos estructuras [MAPIUID](mapiuid.md) para determinar si contienen el mismo identificador. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |**MAPIUID** <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a>Sintaxis

 _lpuid1_
  
> Puntero a la primera estructura **MAPIUID** que se probará. 
    
 _lpuid2_
  
> Puntero a la segunda estructura **MAPIUID** que se probará. 
    
## <a name="remarks"></a>Notas

La macro **IsEqualMAPIUID** devuelve TRUE si las dos estructuras **MAPIUID** contienen el mismo identificador y FALSE si no lo hace. 
  
La macro **IsEqualMAPIUID** requiere que el archivo de encabezado Memory.h se incluirán. 
  
## <a name="see-also"></a>Ver también



[MAPIUID](mapiuid.md)


[Macros relacionadas con las estructuras](macros-related-to-structures.md)

