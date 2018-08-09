---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Modifica el orden de la categoría especificada de cuentas.
ms.openlocfilehash: fcb27404471c9b551320027b0ed6979926ad3d58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816226"
---
# <a name="iolkaccountmanagersetorder"></a>IOlkAccountManager::SetOrder

Modifica el orden de la categoría especificada de cuentas.
  
## <a name="quick-info"></a>Información rápida

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a>Parámetros

_pclsidCategory_
  
> [entrada] El identificador de clase de categoría para la que se va a establecer el orden. El valor debe ser uno de estos procedimientos:
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_cAccts_
  
> [entrada] El número de cuentas.
    
_rgAccts_
  
> [entrada] Una matriz de identificadores de cuenta. El tamaño de la matriz es _cAccts_.
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
|E_ACCT_WRONG_SORT_ORDER  <br/> |El nuevo criterio de ordenación tiene un número diferente de las cuentas que el criterio de ordenación anterior.  <br/> |
|E_INVALIDARG  <br/> |Uno o más argumentos no son válidos.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |No se ha inicializado el Administrador de cuentas para su uso.  <br/> |
   
## <a name="remarks"></a>Notas

El autor de la llamada asigna memoria para el puntero de matriz _prgAccts_ así como para la matriz en qué momentos _prgAccts_ . 
  
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)  
- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

