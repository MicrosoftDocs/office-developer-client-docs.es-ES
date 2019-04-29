---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Notifica al cliente los cambios en la cuenta especificada.
ms.openlocfilehash: 269d8a8bd605c9d8a0a4057e87895522d8587ee9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424570"
---
# <a name="iolkaccountnotifynotify"></a>IOlkAccountNotify::Notify

Notifica al cliente los cambios en la cuenta especificada.
  
## <a name="quick-info"></a>Información rápida

Consulte [IOlkAccountNotify](iolkaccountnotify.md).
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>Parameters

_dwNotify_
  
> a El tipo de notificación. El valor debe ser uno de los siguientes:
    
   - NOTIFY_ACCT_CHANGED 
    
   - NOTIFY_ACCT_CREATED 
    
   - NOTIFY_ACCT_DELETED
    
   - NOTIFY_ACCT_ORDER_CHANGED 
    
   - NOTIFY_ACCT_PREDELETED 
    
 _dwAcctID_
  
> a El identificador de cuenta de la cuenta que se ha creado, cambiado, eliminado o eliminado previamente.
    
 _dwFlags_
  
>  a No se usa. OLK_ACCOUNT_NO_FLAGS es el único valor admitido. 
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="see-also"></a>Ver también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)  
- [IOlkAccountManager](iolkaccountmanager.md)

