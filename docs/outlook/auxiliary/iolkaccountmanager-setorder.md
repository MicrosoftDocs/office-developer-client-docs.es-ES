---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Modifica el orden de la categoría de cuentas especificada.
ms.openlocfilehash: 29dfe4fd1bda9e323481297167361650c3b3a173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422862"
---
# <a name="iolkaccountmanagersetorder"></a>IOlkAccountManager::SetOrder

Modifica el orden de la categoría de cuentas especificada.
  
## <a name="quick-info"></a>Información rápida

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a>Parameters

_pclsidCategory_
  
> a IDENTIFICADOR de clase de categoría para el que se va a establecer el orden. El valor debe ser uno de los siguientes:
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_cAccts_
  
> a El número de cuentas.
    
_rgAccts_
  
> a Una matriz de identificadores de cuenta. El tamaño de la matriz es _cAccts_.
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
|E_ACCT_WRONG_SORT_ORDER  <br/> |El nuevo criterio de ordenación tiene un número de cuentas distinto del criterio de ordenación anterior.  <br/> |
|E_INVALIDARG  <br/> |Uno o más argumentos no son válidos.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |No se ha inicializado el Administrador de cuentas para su uso.  <br/> |
   
## <a name="remarks"></a>Comentarios

El autor de la llamada asigna memoria para el puntero de matriz _prgAccts_ , así como para la matriz en la que apunta _prgAccts_ . 
  
## <a name="see-also"></a>Ver también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)  
- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

