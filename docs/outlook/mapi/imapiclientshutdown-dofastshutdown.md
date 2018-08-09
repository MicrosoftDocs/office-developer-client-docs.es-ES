---
title: IMAPIClientShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: 310cba9a-a343-484d-a029-fcd51b731460
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 447832d88a9740875fcf39a32adcf4ebb99e05ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817198"
---
# <a name="imapiclientshutdowndofastshutdown"></a>IMAPIClientShutdown::DoFastShutdown

  
  
**Hace referencia a**: Outlook 
  
Indica la intención del cliente MAPI para salir inmediatamente el proceso de cliente.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Valor devuelto

S_OK
  
> El subsistema MAPI ha indicado a proveedores MAPI cargados que el cliente MAPI está saliendo inmediatamente, y los proveedores de MAPI están listos para la salida del cliente.
    
MAPI_E_NO_SUPPORT
  
> El subsistema MAPI no admite el apagado rápido de cliente.
    
## <a name="remarks"></a>Comentarios

Para evitar la pérdida de datos desde el apagado rápido de un cliente MAPI, los clientes MAPI deben llamar a los métodos [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) y **IMAPIClientShutdown::DoFastShutdown** según el resultado S_OK devuelto por el subsistema MAPI en el método [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . Para obtener más información, vea [Procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Vea también



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Cierre del cliente de MAPI](client-shutdown-in-mapi.md)

