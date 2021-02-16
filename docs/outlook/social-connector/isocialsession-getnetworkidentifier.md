---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Obtiene una cadena que representa un identificador de red social único para una conexión de red social determinada.
ms.openlocfilehash: 3051abd6dcccec878e8c53332980731772d543eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433279"
---
# <a name="isocialsessiongetnetworkidentifier"></a>ISocialSession::GetNetworkIdentifier

Obtiene una cadena que representa un identificador de red social único para una conexión de red social determinada. 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a>Parámetros

_networkIdentifier_
  
> [salida] Cadena que contiene un identificador de red social único.
    
## <a name="remarks"></a>Comentarios

Un identificador de red único es una cadena que identifica la red social del proveedor de Outlook Social Connector (OSC). Este método también puede devolver E_NOTIMPL.
  
## <a name="see-also"></a>Consulte también

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

