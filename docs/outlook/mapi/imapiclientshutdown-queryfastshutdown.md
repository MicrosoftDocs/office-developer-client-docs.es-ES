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
ms.openlocfilehash: 6a76488f56f9d1eb1b344c01de2615627dd5d3ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418151"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a>IMAPIClientShutdown::QueryFastShutdown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Consulta el subsistema MAPI para obtener compatibilidad con el apagado rápido que proporcionan los proveedores MAPI cargados.
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Valor devuelto

S_OK
  
> El subsistema MAPI admite el cliente MAPI para el apagado rápido.
    
MAPI_E_NO_SUPPORT
  
> El proveedor MAPI no es compatible con el cliente MAPI para el apagado rápido.
    
## <a name="remarks"></a>Comentarios

El hecho de que el subsistema MAPI admita el cliente MAPI para el apagado rápido depende de la configuración del registro de Windows del usuario o del comportamiento predeterminado del cliente MAPI para el apagado rápido. También depende de la capacidad de los proveedores MAPI cargados para admitir el apagado rápido. Para obtener más información, consulte [Opciones de usuario de apagado rápido](fast-shutdown-user-options.md).
  
## <a name="see-also"></a>Ver también



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Cierre del cliente en MAPI](client-shutdown-in-mapi.md)

