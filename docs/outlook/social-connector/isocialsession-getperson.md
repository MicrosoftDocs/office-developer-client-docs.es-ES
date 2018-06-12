---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Obtiene una interfaz ISocialPerson basándose en el parámetro userID.
ms.openlocfilehash: 5769f4c41bb97f45ab722f1b3a3febe24c8a7ab2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821116"
---
# <a name="isocialsessiongetperson"></a>ISocialSession::GetPerson

Obtiene una interfaz [ISocialPerson](isocialpersoniunknown.md) basándose en el parámetro _userID_ . 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a>Sintaxis

_userId_
  
> [entrada] Una cadena que contiene una dirección SMTP o identificador de usuario de una persona.
    
_resultado_
  
> [out] Una interfaz **ISocialPerson** . 
    
## <a name="remarks"></a>Notas

El parámetro _userID_ debe ser una dirección SMTP o identificador de usuario. 
  
## <a name="see-also"></a>Ver también

- [ISocialSession: IUnknown](isocialsessioniunknown.md)

