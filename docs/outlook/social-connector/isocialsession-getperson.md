---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Obtiene una interfaz ISocialPerson basada en el parámetro userID.
ms.openlocfilehash: b54e39b3712fb57d89d03787f1e5fa0ff50ff84a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439824"
---
# <a name="isocialsessiongetperson"></a>ISocialSession::GetPerson

Obtiene una [interfaz ISocialPerson](isocialpersoniunknown.md) basada en el _parámetro userID._ 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a>Parameters

_userId_
  
> [in] Cadena que contiene un identificador de usuario o una dirección SMTP de una persona.
    
_result_
  
> [salida] Una **interfaz ISocialPerson.** 
    
## <a name="remarks"></a>Comentarios

El  _parámetro userID_ debe ser un identificador de usuario o una dirección SMTP. 
  
## <a name="see-also"></a>Vea también

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

