---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Notifica al cliente de los cambios realizados en la cuenta especificada.
ms.openlocfilehash: ea4cab8cb8571cf5f34637c08935c78c657e5503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816243"
---
# <a name="iolkaccountnotifynotify"></a>IOlkAccountNotify::Notify

Notifica al cliente de los cambios realizados en la cuenta especificada.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccountNotify](iolkaccountnotify.md).
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>Parámetros

_dwNotify_
  
> [entrada] El tipo de notificación. El valor debe ser uno de estos procedimientos:
    
   - NOTIFY_ACCT_CHANGED 
    
   - NOTIFY_ACCT_CREATED 
    
   - NOTIFY_ACCT_DELETED
    
   - NOTIFY_ACCT_ORDER_CHANGED 
    
   - NOTIFY_ACCT_PREDELETED 
    
 _dwAcctID_
  
> [entrada] El identificador de cuenta de la cuenta que se ha creado, modificado, eliminado o eliminado previamente.
    
 _dwFlags_
  
>  [entrada] No se usa. OLK_ACCOUNT_NO_FLAGS es el único valor admitido. 
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)  
- [IOlkAccountManager](iolkaccountmanager.md)

