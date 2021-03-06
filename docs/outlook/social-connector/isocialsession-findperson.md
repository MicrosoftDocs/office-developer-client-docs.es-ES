---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Obtiene una cadena que representa una o varias personas que coinciden con el parámetro userID.
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434798"
---
# <a name="isocialsessionfindperson"></a>ISocialSession::FindPerson

Obtiene una cadena que representa una o varias personas que coinciden con el _parámetro userID._ 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a>Parameters

_userId_
  
> [in] Id. de usuario de red social, dirección SMTP o nombre para mostrar de una persona.
    
_result_
  
> [salida] Una cadena XML que representa una o varias personas que coinciden con la información de identificación especificada por el _parámetro userId._ 
    
## <a name="remarks"></a>Comentarios

Si una o más personas coinciden con la **solicitud FindPerson,** este método devuelve la información de esas personas en el _parámetro result._ La _cadena_ XML de resultado debe cumplir con la definición de esquema para amigos **,** tal como se define en el esquema para la extensibilidad del proveedor Outlook Social Connector (OSC). 
  
## <a name="see-also"></a>Vea también

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

