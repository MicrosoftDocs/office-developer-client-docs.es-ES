---
title: IOlkAccountManagerEnumerateAccounts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: Obtiene un enumerador para las cuentas de la categoría específica o tipo.
ms.openlocfilehash: d0d383dee0e76dd6310d01bd1482e307c2374856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423051"
---
# <a name="iolkaccountmanagerenumerateaccounts"></a>IOlkAccountManager::EnumerateAccounts

Obtiene un enumerador para las cuentas de la categoría específica o tipo.
  
## <a name="quick-info"></a>Información rápida

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::EnumerateAccounts (  
    const CLSID *pclsidCategory, 
    const CLSID *pclsidType, 
    DWORD dwFlags, 
    IOlkEnum **ppEnum 
);

```

## <a name="parameters"></a>Parámetros

_pclsidCategory_
  
> [entrada] El identificador de clase de la categoría para enumerar. El valor debe ser uno de estos procedimientos:
    
   - CLSID_OlkMail 
    
   -  CLSID_OlkAddressBook 
    
   - CLSID_OlkStore 
    
_pclsidType_
  
> [entrada] El identificador de clase del tipo de cuenta para enumerar. El valor debe ser uno de estos procedimientos:
    
   - CLSID_OlkPOP3Account
    
   - CLSID_OlkIMAP4Account
    
   - CLSID_OlkMAPIAccount
    
   - CLSID_OlkHotmailAccount
    
   - CLSID_OlkLDAPAccount
    
_dwFlags_
  
> [entrada] Marcadores para modificar el comportamiento. El único valor admitido es OLK_ACCOUNT_NO_FLAGS.
    
_ppEnum_
  
> [out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface. 
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |No se ha inicializado el Administrador de cuentas para su uso.  <br/> |
   
## <a name="remarks"></a>Comentarios

Especificar NULL para la categoría, devuelve un enumerador de todas las cuentas del tipo especificado. De forma similar, si se especifica NULL para el tipo de, devuelve un enumerador de todas las cuentas de la categoría especificada.
  
 **IOlkAccountManager::EnumerateAccounts** no es compatible con la categoría de la libreta de direcciones para una cuenta de Exchange. Si la cuenta es una cuenta de Exchange (*pclsidType*  es **CLSID_OlkMAPIAccount** ), y está intentando enumerar cuentas que implementan la libreta de direcciones (*prgclsidCategory*  es **CLSID_OlkAddressBook** ), al llamar a **IOlkAccountManager::EnumerateAccounts** no se devolverá la cuenta de Exchange en el enumerador de cuentas  *ppEnum*  . 
  
## <a name="see-also"></a>Consulte también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)  
- [IOlkEnum](iolkenum.md)

