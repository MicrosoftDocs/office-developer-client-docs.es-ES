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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: d9f08c13f68c7d3d9f41b9a67ac1888d6c507c34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817455"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**Se aplica a**: Outlook 
  
Las consultas que admite el proveedor MAPI de apagado rápido. 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Valor devuelto

S_OK
  
> El proveedor MAPI es compatible con el cliente MAPI para rapidez en el cierre.
    
MAPI_E_NO_SUPPORT
  
> El proveedor MAPI no es compatible con el cliente MAPI para rapidez en el cierre.
    
## <a name="remarks"></a>Notas

Proveedores MAPI que no es necesario para admitir el apagado rápido cliente aún deben implementar la interfaz [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) y tener el método **IMAPIProviderShutdown::QueryFastShutdown** devolver MAPI_E_NO_SUPPORT. Para Outlook como un cliente MAPI, esto hace que Outlook que se debe esperar para que todas las referencias externas a liberarse antes de que exista. 
  
Dependiendo del registro de Windows del usuario configuración de apagado rápido, no se implementa la interfaz **IMAPIProviderShutdown** no impide necesariamente un apagado rápido de cliente. 
  
## <a name="see-also"></a>Ver también



[IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md)


[Cierre del cliente de MAPI](client-shutdown-in-mapi.md)

