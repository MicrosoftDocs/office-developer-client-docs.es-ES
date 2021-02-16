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
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4ff93ed9353d58ef6b68823bebf8b5b27a0df6e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428847"
---
# <a name="imapiprovidershutdowndofastshutdown"></a>IMAPIProviderShutdown::DoFastShutdown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica al proveedor MAPI que el cliente MAPI sale inmediatamente, de modo que el proveedor MAPI conservará los cambios para evitar la pérdida de datos.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Valor devuelto

S_OK
  
> El proveedor MAPI está listo para que el cliente MAPI salga inmediatamente. 
    
## <a name="see-also"></a>Consulte también



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Cierre del cliente en MAPI](client-shutdown-in-mapi.md)

