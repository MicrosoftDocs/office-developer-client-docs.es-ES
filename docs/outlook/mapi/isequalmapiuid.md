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
ms.openlocfilehash: 0c72164cac8a37d0372ac93f4ed6d3face966ddb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566666"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Prueba dos estructuras [MAPIUID](mapiuid.md) para determinar si contienen el mismo identificador. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |**MAPIUID** <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a>Parámetros

 _lpuid1_
  
> Puntero a la primera estructura **MAPIUID** que se probará. 
    
 _lpuid2_
  
> Puntero a la segunda estructura **MAPIUID** que se probará. 
    
## <a name="remarks"></a>Comentarios

La macro **IsEqualMAPIUID** devuelve TRUE si las dos estructuras **MAPIUID** contienen el mismo identificador y FALSE si no lo hace. 
  
La macro **IsEqualMAPIUID** requiere que el archivo de encabezado Memory.h se incluirán. 
  
## <a name="see-also"></a>Recursos adicionales



[MAPIUID](mapiuid.md)


[Macros relacionadas con estructuras](macros-related-to-structures.md)

