---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Registra a un cliente con el Administrador de cuentas para las notificaciones con respecto a todas las cuentas.
ms.openlocfilehash: 1fb697fef44b9ed32888527c3c9e467be69ba4c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816216"
---
# <a name="iolkaccountmanageradvise"></a>IOlkAccountManager::Advise

Registra a un cliente con el Administrador de cuentas para las notificaciones con respecto a todas las cuentas.
  
## <a name="quick-info"></a>Información rápida

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a>Parámetros

_pNotify_
  
> [entrada] Una interfaz de [IOlkAccountNotify](iolkaccountnotify.md) que va a usar el Administrador de cuentas para enviar las notificaciones para el cliente. 
    
_pdwCookie_
  
> [out] Una cookie que va a usar [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) al quitar el registro de la cuenta. 
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
|E_INVALIDARG  <br/> |Se ha proporcionado un argumento no válido.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |No se ha inicializado el Administrador de cuentas para su uso.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)  
- [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md)

