---
title: IMAPIClientShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: b743b5b6-4a7c-46b8-99eb-afd13ee947db
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 784a2f497811ba7c4ba0abf260ff32fde75de76a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584936"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a>IMAPIClientShutdown::QueryFastShutdown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las consultas admiten el subsistema MAPI para apagado rápido proporcionado por proveedores MAPI cargados.
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Valor devuelto

S_OK
  
> El subsistema MAPI es compatible con el cliente MAPI para rapidez en el cierre.
    
MAPI_E_NO_SUPPORT
  
> El proveedor MAPI no es compatible con el cliente MAPI para rapidez en el cierre.
    
## <a name="remarks"></a>Comentarios

Si el subsistema MAPI es compatible con el cliente MAPI de cierre rápido depende de configuración de registro de Windows del usuario o el comportamiento predeterminado del cliente MAPI de apagado rápido. También depende de la capacidad de los proveedores MAPI cargados para admitir apagado rápido. Para obtener más información, vea [Opciones de usuario de apagado Fast](fast-shutdown-user-options.md).
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Cierre del cliente de MAPI](client-shutdown-in-mapi.md)

