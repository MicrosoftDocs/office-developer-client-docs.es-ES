---
title: IMAPIOfflineGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCapabilities
api_type:
- COM
ms.assetid: aa8dc48b-9e1c-8da0-9579-10b7174e99de
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 48d59d17d81da2ae78348a57ad8b1cb75486b1a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433377"
---
# <a name="imapiofflinegetcapabilities"></a>IMAPIOffline::GetCapabilities

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Obtiene las condiciones para las que un objeto sin conexión admite las devoluciones de llamada.
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>Parameters

 _pulCapablities_
  
> [salida] Máscara de bits de las siguientes marcas de funcionalidad:
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> El objeto sin conexión es capaz de proporcionar notificaciones sin conexión.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> El objeto sin conexión es capaz de proporcionar notificaciones en línea.
    
## <a name="remarks"></a>Comentarios

Al abrir un objeto sin conexión mediante **[HrOpenOfflineObj,](hropenofflineobj.md)** un cliente puede consultar en [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) para obtener un puntero a una interfaz **IMAPIOffline** y llamar a **IMAPIOffline::GetCapabilities** para averiguar las devoluciones de llamada admitidas por el objeto. A continuación, el cliente puede elegir configurar las devoluciones de llamada **mediante IMAPIOfflineMgr**.
  
Tenga en cuenta que, según el servidor de correo de un objeto sin conexión, un objeto que admite devoluciones de llamada para ponerse en línea no admite necesariamente devoluciones de llamada para desconectarse.
  
Tenga en cuenta también que, aunque un objeto sin conexión puede admitir devoluciones de llamada para cambios distintos de online/offline, la API de estado sin conexión solo admite cambios en línea o sin conexión, y los clientes deben comprobar solo dichas funcionalidades.
  
## <a name="see-also"></a>Vea también



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

