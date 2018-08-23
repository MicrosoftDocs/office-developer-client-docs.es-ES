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
ms.openlocfilehash: 251359a98f89c88e707e4f705bd94b1f30b32cbd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592055"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a>IMAPIProviderShutdown::NotifyProcessShutdown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica al proveedor MAPI que un cliente MAPI se va a realizar un apagado rápido, por lo que el proveedor puede realizar las acciones para evitar la pérdida de datos.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Valor devuelto

S_OK
  
> El proveedor MAPI está realizando acciones para evitar la pérdida de datos cuando se cierra el cliente MAPI.
    
## <a name="see-also"></a>Recursos adicionales



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Cierre del cliente de MAPI](client-shutdown-in-mapi.md)

