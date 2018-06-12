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
ms.openlocfilehash: 7108a7e42e9b54e069d8d420283c1ebad3367830
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821128"
---
# <a name="isocialprovidergetautoconfiguredsession"></a>ISocialProvider::GetAutoConfiguredSession

Obtiene una interfaz [ISocialSession](isocialsessioniunknown.md) configurada automáticamente. 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>Sintaxis

_sesión_
  
> [out] Una interfaz **ISocialSession** . 
    
## <a name="remarks"></a>Notas

La interfaz devuelta de **ISocialSession** se registra automáticamente a la red, en función de un método que es específico del proveedor. 
  
El proveedor debe devolver el error OSC_E_NOT_IMPLEMENTED si la red social no admite la configuración automática. Para obtener información acerca de los códigos de error, vea [Códigos de Error de Outlook Social Connector proveedor](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Ver también

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

