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
ms.openlocfilehash: 1c66032788758b04558a37a4c35ff4dd6c702fa2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568269"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a>IMAPIClientShutdown::NotifyProcessShutdown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica la intención de continuar con la del cliente MAPI cerrado.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Valor devuelto

S_OK
  
> Ha intentado el subsistema MAPI notificar a los proveedores MAPI cargados que el cliente MAPI se va a realizar un cierre rápido.
    
## <a name="remarks"></a>Comentarios

Para evitar la pérdida de datos desde el apagado rápido de un cliente MAPI, los clientes MAPI deben llamar a los métodos **IMAPIClientShutdown::NotifyProcessShutdown** y [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) según el resultado S_OK devuelto por el subsistema MAPI en el método [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . Para obtener más información, vea [Procedimientos recomendados para el apagado rápido](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Cierre del cliente de MAPI](client-shutdown-in-mapi.md)

