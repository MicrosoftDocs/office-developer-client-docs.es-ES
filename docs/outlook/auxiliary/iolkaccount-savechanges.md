---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Confirma los cambios en el objeto de cuenta escribiendo en el almacén del registro.
ms.openlocfilehash: c23cefbbda62de9b7e159e500d95b8db5ff34ef4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425837"
---
# <a name="iolkaccountsavechanges"></a>IOlkAccount::SaveChanges

Confirma los cambios en el objeto de cuenta escribiendo en el almacén del registro.
  
## <a name="quick-info"></a>Información rápida

Consulte [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Parameters

_dwFlags_
  
> [entrada] Marcadores para modificar el comportamiento. OLK_ACCOUNT_NO_FLAGS es el único valor admitido.
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |El método se realizó correctamente.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |No se encuentra la cuenta especificada.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |No se ha inicializado el Administrador de cuentas para su uso.  <br/> |
   
## <a name="remarks"></a>Comentarios

Después de cambiar el valor de las propiedades de cuenta mediante [IOlkAccount:: SetProp](iolkaccount-setprop.md), use **IOlkAccount:: SaveChanges** para guardar los cambios. 
  
## <a name="see-also"></a>Ver también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md) 
- [IOlkAccountManager::SaveChanges](iolkaccountmanager-savechanges.md)

