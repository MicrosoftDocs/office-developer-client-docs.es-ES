---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Guarda los cambios realizados a la cuenta especificada.
ms.openlocfilehash: 87b513659b632e88697fb63d1aeccccb77ed9fd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816238"
---
# <a name="iolkaccountmanagersavechanges"></a>IOlkAccountManager::SaveChanges

Guarda los cambios realizados a la cuenta especificada.
  
## <a name="quick-info"></a>Información rápida

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Parámetros

_dwAcctID_
  
> [entrada] El identificador de cuenta para guardar. 
    
_dwFlags_
  
> [entrada] Marcadores para modificar el comportamiento. OLK_ACCOUNT_NO_FLAGS es el único valor admitido.
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada se ha realizado correctamente  <br/> |
|E_ACCT_NOT_FOUND  <br/> |No se encuentra la cuenta especificada.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |No se ha inicializado el Administrador de cuentas para su uso.  <br/> |
   
## <a name="remarks"></a>Notas

Después de cambiar el valor de las propiedades de cuenta mediante el uso de [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccountManager::SaveChanges** o [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) para guardar estos cambios. 
  
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md) 
- [IOlkAccount::SaveChanges](iolkaccount-savechanges.md)

