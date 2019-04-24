---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Guarda los cambios realizados en la cuenta especificada.
ms.openlocfilehash: dbb1dffa1725e96bd2ab635341718ce53738b864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322025"
---
# <a name="iolkaccountmanagersavechanges"></a>IOlkAccountManager::SaveChanges

Guarda los cambios realizados en la cuenta especificada.
  
## <a name="quick-info"></a>Información rápida

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Parameters

_dwAcctID_
  
> a IDENTIFICADOR de cuenta que se va a guardar. 
    
_dwFlags_
  
> [entrada] Marcadores para modificar el comportamiento. OLK_ACCOUNT_NO_FLAGS es el único valor admitido.
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada se realizó correctamente  <br/> |
|E_ACCT_NOT_FOUND  <br/> |No se encuentra la cuenta especificada.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |No se ha inicializado el Administrador de cuentas para su uso.  <br/> |
   
## <a name="remarks"></a>Comentarios

Después de cambiar el valor de las propiedades de cuenta mediante [IOlkAccount:: SetProp](iolkaccount-setprop.md), use **IOlkAccountManager:: SaveChanges** o [IOlkAccount:: SaveChanges](iolkaccount-savechanges.md) para guardar los cambios. 
  
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md) 
- [IOlkAccount::SaveChanges](iolkaccount-savechanges.md)

