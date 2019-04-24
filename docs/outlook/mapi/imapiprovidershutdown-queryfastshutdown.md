---
title: IMAPIProviderShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: 12069912-4b87-4945-9123-51106e0d2d54
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 50b49761cf5923b11a450cbce7b7991f5ddd4d82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338489"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Consulta al proveedor MAPI para obtener compatibilidad con el apagado rápido. 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Valor devuelto

S_OK
  
> El proveedor MAPI admite el cierre rápido del cliente MAPI.
    
MAPI_E_NO_SUPPORT
  
> El proveedor MAPI no es compatible con el cliente MAPI para el apagado rápido.
    
## <a name="remarks"></a>Comentarios

Los proveedores MAPI que no necesitan admitir el apagado rápido de cliente deben seguir implementando la interfaz [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) y tienen el método **IMAPIProviderShutdown:: QueryFastShutdown** devuelve MAPI_E_NO_SUPPORT. Para Outlook como cliente MAPI, esto hace que Outlook espere a que se liberen todas las referencias externas antes de su salida. 
  
En función de la configuración del registro de Windows del usuario para el apagado rápido, no implementar la interfaz **IMAPIProviderShutdown** no impide necesariamente un apagado rápido del cliente. 
  
## <a name="see-also"></a>Vea también



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Cierre del cliente en MAPI](client-shutdown-in-mapi.md)

