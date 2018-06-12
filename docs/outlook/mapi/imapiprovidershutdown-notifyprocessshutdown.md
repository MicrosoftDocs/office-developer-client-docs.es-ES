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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: cce98dc630dd9f7fa459ca31d94d012ba9a7fd85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817429"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a>IMAPIProviderShutdown::NotifyProcessShutdown

  
  
**Se aplica a**: Outlook 
  
Indica al proveedor MAPI que un cliente MAPI se va a realizar un apagado rápido, por lo que el proveedor puede realizar las acciones para evitar la pérdida de datos.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Valor devuelto

S_OK
  
> El proveedor MAPI está realizando acciones para evitar la pérdida de datos cuando se cierra el cliente MAPI.
    
## <a name="see-also"></a>Ver también



[IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md)


[Cierre del cliente de MAPI](client-shutdown-in-mapi.md)

