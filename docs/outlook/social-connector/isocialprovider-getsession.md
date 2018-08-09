---
title: ISocialProviderGetSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 371b48c5-6d77-4d2d-890c-bb234c7eaabc
description: Obtiene una interfaz ISocialSession.
ms.openlocfilehash: 59e6f61e1954f64d875c6336b211dcb530100252
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821122"
---
# <a name="isocialprovidergetsession"></a>ISocialProvider::GetSession

Obtiene una interfaz [ISocialSession](isocialsessioniunknown.md) . 
  
```cpp
HRESULT _stdcall GetSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>Parámetros

_session_
  
> [salida] Una interfaz **ISocialSession**. 
    
## <a name="remarks"></a>Comentarios

Outlook Social Connector (OSC), se usa la interfaz **ISocialSession** para iniciar sesión en la red social. 
  
## <a name="see-also"></a>Vea también

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

