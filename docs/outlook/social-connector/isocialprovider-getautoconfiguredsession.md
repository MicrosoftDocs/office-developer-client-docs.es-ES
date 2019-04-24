---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: Obtiene una interfaz ISocialSession configurada automáticamente.
ms.openlocfilehash: 34f048158a484612b92bcd2750401caecda64ba2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285782"
---
# <a name="isocialprovidergetautoconfiguredsession"></a>ISocialProvider::GetAutoConfiguredSession

Obtiene una interfaz [ISocialSession](isocialsessioniunknown.md) configurada automáticamente. 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>Parámetros

_session_
  
> [salida] Una interfaz **ISocialSession**. 
    
## <a name="remarks"></a>Comentarios

La interfaz **ISocialSession** devuelta se registra automáticamente en la red, basándose en un método específico para el proveedor. 
  
El proveedor debe devolver el error OSC_E_NOT_IMPLEMENTED si la red social no admite la configuración automática. Para obtener información sobre códigos de error, vea [Códigos de error del proveedor Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Vea también

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

