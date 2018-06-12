---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Obtiene una cadena que representa un identificador único de redes sociales para una conexión de red social determinado.
ms.openlocfilehash: eb618ba8e8bb37278c1fdb09d984fba141a9d686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821240"
---
# <a name="isocialsessiongetnetworkidentifier"></a>ISocialSession::GetNetworkIdentifier

Obtiene una cadena que representa un identificador único de redes sociales para una conexión de red social determinado. 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a>Sintaxis

_networkIdentifier_
  
> [out] Una cadena que contiene un identificador único de redes sociales.
    
## <a name="remarks"></a>Notas

Un identificador único de red es una cadena que identifica la red social del proveedor de Outlook Social Connector (OSC). Este método también puede devolver E_NOTIMPL.
  
## <a name="see-also"></a>Ver también

- [ISocialSession: IUnknown](isocialsessioniunknown.md)

