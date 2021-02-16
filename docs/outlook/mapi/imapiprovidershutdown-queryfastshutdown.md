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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418221"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Consulta al proveedor MAPI la compatibilidad con el apagado rápido. 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Valor devuelto

S_OK
  
> El proveedor MAPI admite que el cliente MAPI realice un apagado rápido.
    
MAPI_E_NO_SUPPORT
  
> El proveedor MAPI no admite el cliente MAPI para realizar el apagado rápido.
    
## <a name="remarks"></a>Comentarios

Los proveedores MAPI que no necesitan admitir el apagado rápido del cliente deben seguir implementando la interfaz [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) y hacer que el método **IMAPIProviderShutdown::QueryFastShutdown** devuelva MAPI_E_NO_SUPPORT. Para Outlook como cliente MAPI, esto hace que Outlook espere a que se liberarán todas las referencias externas antes de salir. 
  
Según la configuración del Registro de Windows del usuario para el apagado rápido, no implementar la interfaz **IMAPIProviderShutdown** no impide necesariamente un apagado rápido del cliente. 
  
## <a name="see-also"></a>Consulte también



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Cierre del cliente en MAPI](client-shutdown-in-mapi.md)

