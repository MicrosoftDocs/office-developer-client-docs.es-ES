---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifica a un usuario que puede o no tener datos de disponibilidad disponibles.
ms.openlocfilehash: 2511a94678f9ef8f2cb6be868db4f718d92ecb6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317664"
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

## <a name="members"></a>Miembros

_m_cbEid_
  
> La longitud del identificador de entrada del usuario de correo, tal como se representa en la interfaz [IMailUser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) . 
    
_m_lpEid_
  
> IDENTIFICADOR de entrada del usuario de correo, tal como se representa en la interfaz **IMailUser** . 
    
_m_ulReserved_
  
> Este parámetro está reservado para uso interno de Outlook y no es compatible.
    
_m_pwszReserved_
  
> Este parámetro está reservado para uso interno de Outlook y no es compatible.
    
## <a name="see-also"></a>Vea también

- [Acerca de la API de disponibilidad](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

