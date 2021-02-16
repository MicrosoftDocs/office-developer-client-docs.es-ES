---
title: IMAPIProviderShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: a00d71b1-d705-40d5-b667-f91b57db85da
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4b18cfc2191ffee936e1056d9bb656a7ad7dd3ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405250"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a>IMAPIProviderShutdown::NotifyProcessShutdown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica al proveedor MAPI que un cliente MAPI va a realizar un apagado rápido, de modo que el proveedor puede realizar acciones para evitar la pérdida de datos.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Valor devuelto

S_OK
  
> El proveedor MAPI está llevando a cabo acciones para evitar la pérdida de datos cuando se cierra el cliente MAPI.
    
## <a name="see-also"></a>Consulte también



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Cierre del cliente en MAPI](client-shutdown-in-mapi.md)

