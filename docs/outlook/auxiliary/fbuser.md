---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifica a un usuario que puede o no tener datos de disponibilidad disponibles.
ms.openlocfilehash: edfc9980445fcc2e111045650667d93bffa94153
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565140"
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
  
> La longitud del identificador de entrada de usuario de correo, tal como está representado por la interfaz [IMailUser](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) . 
    
_m_lpEid_
  
> El identificador de entrada del usuario de correo, tal como está representado por la interfaz **IMailUser** . 
    
_m_ulReserved_
  
> Este parámetro está reservado para uso interno de Outlook y no se admite.
    
_m_pwszReserved_
  
> Este parámetro está reservado para uso interno de Outlook y no se admite.
    
## <a name="see-also"></a>Recursos adicionales

- [Información sobre la API de disponibilidad](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

