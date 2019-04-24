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
ms.openlocfilehash: 183e47bea70ed378947afb6a1d0e5561fb9307f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331671"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

Determina si los usuarios especificados son amigos.
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>Parameters

_userIds_
  
> a Estructura que especifica una matriz de valores de identificador de usuario que corresponden a un conjunto de personas en la red social.
    
_obtener_
  
> contempla Puntero a estructura que especifica una matriz de valores booleanos, que indica si la persona correspondiente de __ la matriz de identificadores de usuario es un amigo. 
    
## <a name="remarks"></a>Comentarios

Para cada persona representada en la matriz de __ entrada del parámetro userids, este método establece el elemento correspondiente en la matriz de salida del parámetro _Results_ . **true** indica que la persona es un amigo y **false** indica que la persona no es una amiga. 
  
## <a name="see-also"></a>Vea también

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

