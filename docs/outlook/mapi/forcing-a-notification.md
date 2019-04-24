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
ms.openlocfilehash: 54eaf9e67da1b520896122c937508a90700a0b84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328101"
---
# <a name="forcing-a-notification"></a>Forzar una notificación

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando los proveedores de servicios usan los métodos [IMAPISupport: IUnknown](imapisupportiunknown.md) para la notificación, MAPI entrega las notificaciones usando una ventana oculta y su procedimiento de ventana correspondiente. Para que cada proceso reciba una notificación, MAPI envía un mensaje especial a la ventana oculta. Este mensaje se denomina con la constante **szMAPINotificationMsg** que se define en MAPIDEFS. H. 
  
Estas notificaciones se reciben cuando el procedimiento de ventana de la ventana oculta procesa el mensaje **szMAPINotificationMsg** . Para garantizar que se entreguen las notificaciones, es necesario esperar y distribuir este mensaje de **szMAPINotificationMsg** . La implementación de la lógica para lograr esto puede realizarse de forma bastante sencilla, pero MAPI proporciona un punto de entrada a la DLL de MAPI denominado [HrDispatchNotifications](hrdispatchnotifications.md) para que el procesamiento sea incluso más sencillo. Llame a **HrDispatchNotifications** de la siguiente manera para recibir notificaciones en el cliente: 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


