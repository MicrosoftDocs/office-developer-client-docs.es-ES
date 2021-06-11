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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412565"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

Determina si los usuarios especificados son amigos.
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>Parameters

_userIds_
  
> [in] Estructura que especifica una matriz de valores de id. de usuario que corresponden a un conjunto de personas en la red social.
    
_resultados_
  
> [salida] Puntero a la estructura que especifica una matriz de valores booleanos, que indica si la persona correspondiente de la matriz  _userIds_ es un amigo. 
    
## <a name="remarks"></a>Comentarios

Para cada persona representada en la matriz de entrada del parámetro _userIds,_ este método establece el elemento correspondiente en la matriz de salida del _parámetro results._ **true** indica que la persona es un amigo y **false** indica que la persona no es un amigo. 
  
## <a name="see-also"></a>Vea también

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

