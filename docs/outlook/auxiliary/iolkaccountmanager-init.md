---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Inicializa el administrador de cuentas para su uso.
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322039"
---
# <a name="iolkaccountmanagerinit"></a>IOlkAccountManager::Init

Inicializa el administrador de cuentas para su uso.
  
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
  
> [entrada] Una [interfaz IOlkAccountHelper](iolkaccounthelper.md) que proporciona funcionalidad auxiliar de cuenta. 
    
_dwFlags_
  
> [entrada] Marcadores para modificar el comportamiento.
    
   - **ACCT_INIT_NO_STORES_CHECK:** impide que una cuenta (como una cuenta IMAP) se sincronice con un almacén asociado. 
    
   - **ACCT_INIT_NOSYNCH_MAPI_ACCTS:** impide que los servicios MAPI se sincronicen con las cuentas. 
   
   - **ACCT_INIT_NO_NOTIFICATIONS:** impide que el Administrador de cuentas intercepte los mensajes de difusión destinados a otras aplicaciones. 
   
   - **OLK_ACCOUNT_NO_FLAGS:** sincroniza los servicios MAPI con las cuentas. 
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |Ya se ha llamado a **Init.**  <br/> |
|E_OLK_REGISTRY  <br/> |El administrador de cuentas no pudo tener acceso a la configuración del Registro necesaria.  <br/> |
   
## <a name="remarks"></a>Comentarios

El cliente debe llamar a **IOlkAccountManager::Init** para inicializar el administrador de cuentas antes de usar el administrador de cuentas para acceder a cuentas o configurar notificaciones. Dado que Outlook sincroniza automáticamente los servicios MAPI con las cuentas **en** el inicio, use ACCT_INIT_NOSYNCH_MAPI_ACCTS a menos que haya una causa específica para sincronizar. 
  
## <a name="see-also"></a>Consulte también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

