---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Busca una cuenta por valor de propiedad.
ms.openlocfilehash: d09bce88413f85ee3ccc332c3cb88bb545a0ccaf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322081"
---
# <a name="iolkaccountmanagerfindaccount"></a>IOlkAccountManager::FindAccount

Busca una cuenta por valor de propiedad.
  
## <a name="quick-info"></a>Información rápida

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a>Parameters

_dwProp_
  
> a Propiedad en la que se va a realizar la búsqueda. Debe ser [PROP_ACCT_ID](prop_acct_id.md) o [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).
    
_pVar_
  
> a El valor que debe coincidir.
    
_ppAccount_
  
> contempla Se ha encontrado la cuenta. Este objeto admite una interfaz [IOlkAccount](iolkaccount.md) . 
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |No se encuentra la cuenta especificada.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |No se ha inicializado el Administrador de cuentas para su uso.  <br/> |
|E_OLK_PARAM_NOT_SUPPORTED  <br/> |Uno o más parámetros no son válidos.  <br/> |
   
## <a name="see-also"></a>Vea también

- [ACCT_VARIANT](acct_variant.md)  
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)  
- [IOlkAccountHelper](iolkaccounthelper.md)

