---
title: IMAPIProviderShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: d2b66a8e-2e28-4c32-af95-38d345c7bbd7
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 7c38f0650315495875357862f5fa7fe138d2c61b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817408"
---
# <a name="imapiprovidershutdowndofastshutdown"></a>IMAPIProviderShutdown::DoFastShutdown

  
  
**Se aplica a**: Outlook 
  
Indica que el proveedor MAPI que el cliente MAPI está saliendo inmediatamente, para que el proveedor MAPI guardará los cambios para evitar la pérdida de datos.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Valor devuelto

S_OK
  
> El proveedor MAPI está listo para el cliente de MAPI salir inmediatamente. 
    
## <a name="see-also"></a>Ver también



[IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md)


[Cierre del cliente de MAPI](client-shutdown-in-mapi.md)

