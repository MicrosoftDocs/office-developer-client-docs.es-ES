---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifica a un usuario que puede o no tener datos de disponibilidad disponibles.
ms.openlocfilehash: e83689e28f5fb6e1eae28d760bb57f5ad3796f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816061"
---
# <a name="fbuser"></a>FBUser

Identifica a un usuario que puede o no tener datos de disponibilidad disponibles.
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a>Members

_m_cbEid_
  
> La longitud del identificador de entrada de usuario de correo, tal como está representado por la interfaz [IMailUser](http://msdn.microsoft.com/library/wab._wab_IMailUser%28Office.15%29.aspx) . 
    
_m_lpEid_
  
> El identificador de entrada del usuario de correo, tal como está representado por la interfaz **IMailUser** . 
    
_m_ulReserved_
  
> Este parámetro está reservado para uso interno de Outlook y no se admite.
    
_m_pwszReserved_
  
> Este parámetro está reservado para uso interno de Outlook y no se admite.
    
## <a name="see-also"></a>Vea también

- [Información sobre la API de disponibilidad](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

