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
  
Obtiene las condiciones para las que se admiten las devoluciones de llamada por un objeto sin conexión.
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>Parameters

 _pulCapablities_
  
> contempla Máscara de máscara de las siguientes marcas de capacidad:
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> El objeto sin conexión es capaz de ofrecer notificaciones sin conexión.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> El objeto sin conexión es capaz de ofrecer notificaciones en línea.
    
## <a name="remarks"></a>Comentarios

Al abrir un objeto sin conexión con **[HrOpenOfflineObj](hropenofflineobj.md)**, un cliente puede realizar una consulta en [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) para obtener un puntero a una interfaz de **IMAPIOffline** y llamar a **IMAPIOffline:: GetCapabilities** para conocer las devoluciones de llamada admitidas por el objeto. A continuación, el cliente puede elegir configurar las devoluciones de llamada mediante **IMAPIOfflineMgr**.
  
Tenga en cuenta que, según el servidor de correo de un objeto sin conexión, un objeto que admite las devoluciones de llamada para la conexión no es necesariamente compatible con las devoluciones de llamada para desconectarse.
  
Además, tenga en cuenta que, aunque un objeto sin conexión puede admitir devoluciones de llamada para cambios que no sean en línea o sin conexión, la API de estado sin conexión solo admite cambios en línea o sin conexión, y los clientes deben comprobar solo dichas funciones.
  
## <a name="see-also"></a>Ver también



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

