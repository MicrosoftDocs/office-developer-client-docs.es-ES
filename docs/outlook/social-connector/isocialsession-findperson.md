---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Obtiene un valor de tipo string que representa a una o más personas que coinciden con el parámetro userID.
ms.openlocfilehash: 0b7525f853f7d97a991e2996a4e715cc53756d4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821114"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

Obtiene un valor de tipo string que representa a una o más personas que coinciden con el parámetro _userID_ . 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>Parámetros

_userId_
  
> [entrada] Un identificador de usuario de redes sociales, dirección SMTP o nombre para mostrar de una persona.
    
_resultado_
  
> [out] Una cadena XML que representa a una o más personas que coinciden con la información de identificación especificada por el parámetro _userId_ . 
    
## <a name="remarks"></a>Comentarios

Si una o más personas coincide con la solicitud de **FindPerson** , este método devuelve la información de las personas en el parámetro de _resultado_ . La cadena de _resultado_ XML debe cumplir con la definición del esquema para **amigos**, tal como se define en el esquema para la extensibilidad de proveedor de Outlook Social Connector (OSC). 
  
## <a name="see-also"></a>Vea también

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

