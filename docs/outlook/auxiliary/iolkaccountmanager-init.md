---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Inicializa el Administrador de cuentas para su uso.
ms.openlocfilehash: 621c6a73ab2bcbdff17b87ce15af8b4e0c2e1e24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816220"
---
# <a name="iolkaccountmanagerinit"></a>IOlkAccountManager::Init

Inicializa el Administrador de cuentas para su uso.
  
## <a name="quick-info"></a>Información rápida

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>Parámetros

_pAcctHelper_
  
> [entrada] Una interfaz [IOlkAccountHelper](iolkaccounthelper.md) que proporciona funcionalidad de cuenta auxiliar. 
    
_dwFlags_
  
> [entrada] Marcadores para modificar el comportamiento.
    
   - **ACCT_INIT_NO_STORES_CHECK** : impide que se sincronice con un almacén asociado una cuenta (por ejemplo, una cuenta IMAP). 
    
   - **ACCT_INIT_NOSYNCH_MAPI_ACCTS** : servicios de MAPI impide que de la sincronización con las cuentas. 
    
   - **OLK_ACCOUNT_NO_FLAGS** : servicios de MAPI se sincroniza con las cuentas. 
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |Ya se ha llamado **Init** .  <br/> |
|E_OLK_REGISTRY  <br/> |El Administrador de cuentas no pudo tener acceso a la configuración del registro necesaria.  <br/> |
   
## <a name="remarks"></a>Comentarios

El cliente debe llamar a **IOlkAccountManager::Init** para inicializar la cuenta de administrador antes de usar el Administrador de cuentas para obtener acceso a cuentas o configurar las notificaciones. Debido a que Outlook sincroniza automáticamente servicios MAPI con las cuentas de inicio, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** a menos que haya una causa específica para sincronizar. 
  
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

