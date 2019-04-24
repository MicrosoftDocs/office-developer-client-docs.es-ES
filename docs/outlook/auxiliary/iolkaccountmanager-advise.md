---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Registra un cliente con el administrador de cuentas para las notificaciones relativas a todas las cuentas.
ms.openlocfilehash: 5460d55d906d382ce40ecd3fd9277cf370295680
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322200"
---
# <a name="iolkaccountmanageradvise"></a>IOlkAccountManager::Advise

Registra un cliente con el administrador de cuentas para las notificaciones relativas a todas las cuentas.
  
## <a name="quick-info"></a>Información rápida

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a>Parameters

_pNotify_
  
> a Una interfaz [IOlkAccountNotify](iolkaccountnotify.md) que el administrador de cuentas usará para enviar notificaciones al cliente. 
    
_pdwCookie_
  
> contempla Una cookie que [IOlkAccountManager:: Unadvise](iolkaccountmanager-unadvise.md) usará al quitar el registro de la cuenta. 
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
|E_INVALIDARG  <br/> |Se ha proporcionado un argumento no válido.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |No se ha inicializado el Administrador de cuentas para su uso.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)  
- [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md)

