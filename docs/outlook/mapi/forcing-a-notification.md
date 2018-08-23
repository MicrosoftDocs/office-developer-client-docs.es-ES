---
title: Forzar una notificación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5affce8ab7a8b08019816ad9485641c401dd80c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578776"
---
# <a name="forcing-a-notification"></a>Forzar una notificación

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Uso de proveedores de servicio cuando la [IMAPISupport: IUnknown](imapisupportiunknown.md) métodos de notificación, MAPI ofrece las notificaciones mediante una ventana oculta y su correspondiente procedimiento de ventana. Para que cada proceso recibir una notificación, MAPI envía un mensaje especial a la ventana oculta. Este mensaje se denomina con la constante **szMAPINotificationMsg** que se define en MAPIDEFS. H. 
  
Recibir estas notificaciones cuando el procedimiento de la ventana de la ventana oculta procesa el mensaje **szMAPINotificationMsg** . Para garantizar que las notificaciones se entregan, es necesario esperar para y enviar este mensaje **szMAPINotificationMsg** . Implementar la lógica para realizar esta acción puede realizarse bastante simplemente, pero MAPI proporciona un punto de entrada a la DLL MAPI denominada [HrDispatchNotifications](hrdispatchnotifications.md) para hacer que el procesamiento aún más sencillo. Llamar a **HrDispatchNotifications** como se indica a continuación para recibir notificaciones en su cliente: 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


