---
title: IMAPIClientShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: 42dd7889-5e00-419a-91e7-8350be4efd35
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6eef3047368caca5bd932e19738b1d996c3ff28a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438872"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a>IMAPIClientShutdown::NotifyProcessShutdown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica la intención del cliente MAPI de continuar con el cierre.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Valor devuelto

S_OK
  
> El subsistema MAPI ha intentado notificar a los proveedores MAPI cargados que el cliente MAPI va a realizar un apagado rápido.
    
## <a name="remarks"></a>Comentarios

Para evitar la pérdida de datos del apagado rápido de un cliente MAPI, los clientes MAPI deben llamar a los métodos **IMAPIClientShutdown:: NotifyProcessShutdown** y [IMAPIClientShutdown::D ofastshutdown](imapiclientshutdown-dofastshutdown.md) basándose en el resultado S_OK devuelto por el subsistema MAPI en el método [IMAPIClientShutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . Para obtener más información, vea [procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Ver también



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Cierre del cliente en MAPI](client-shutdown-in-mapi.md)

