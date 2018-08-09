---
title: ISocialProfileAreFriendsOrColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: Determina si los usuarios especificados son amigos.
ms.openlocfilehash: 17e7864dc60bf99df2028e5f6c57f0619d880a8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821099"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

Determina si los usuarios especificados son amigos.
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>Parámetros

_identificadores de usuario_
  
> [entrada] Una estructura que especifica una matriz de valores de identificador de usuario que corresponden a un conjunto de personas en la red social.
    
_resultados_
  
> [out] Un puntero a la estructura que especifica una matriz de valores booleanos, que indica si la persona correspondiente en la matriz de _identificadores de usuario_ es un amigo. 
    
## <a name="remarks"></a>Comentarios

Para cada persona representada en la matriz de entrada del parámetro de _identificadores de usuario_ , este método establece el elemento correspondiente en la matriz de salida del parámetro de _resultados_ . **true** indica que la persona es un amigo y **false** indica que la persona no es un amigo. 
  
## <a name="see-also"></a>Vea también

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

