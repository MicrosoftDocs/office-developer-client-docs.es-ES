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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433286"
---
# <a name="forcing-a-notification"></a><span data-ttu-id="310c3-103">Forzar una notificación</span><span class="sxs-lookup"><span data-stu-id="310c3-103">Forcing a Notification</span></span>

  
  
<span data-ttu-id="310c3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="310c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="310c3-105">Cuando los proveedores de servicios usan los [métodos IMAPISupport : IUnknown](imapisupportiunknown.md) para la notificación, MAPI entrega notificaciones mediante una ventana oculta y su procedimiento de ventana correspondiente.</span><span class="sxs-lookup"><span data-stu-id="310c3-105">When service providers use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods for notification, MAPI delivers notifications using a hidden window and its corresponding window procedure.</span></span> <span data-ttu-id="310c3-106">Para que cada proceso reciba una notificación, MAPI publica un mensaje especial en la ventana oculta.</span><span class="sxs-lookup"><span data-stu-id="310c3-106">For each process to receive a notification, MAPI posts a special message to the hidden window.</span></span> <span data-ttu-id="310c3-107">Este mensaje se denomina con la **constante szMAPINotificationMsg** que se define en MAPIDEFS.H.</span><span class="sxs-lookup"><span data-stu-id="310c3-107">This message is named with the constant **szMAPINotificationMsg** which is defined in MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="310c3-108">Recibirá estas notificaciones cuando el procedimiento de ventana oculta de la ventana procese el **mensaje szMAPINotificationMsg.**</span><span class="sxs-lookup"><span data-stu-id="310c3-108">You receive these notifications when the hidden window's window procedure processes the **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="310c3-109">Para garantizar que las notificaciones se entregan, es necesario esperar y enviar este **mensaje szMAPINotificationMsg.**</span><span class="sxs-lookup"><span data-stu-id="310c3-109">To guarantee that notifications are delivered, it is necessary to wait for and dispatch this **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="310c3-110">La implementación de la lógica para lograr esto se puede hacer de forma bastante sencilla, pero MAPI proporciona un punto de entrada en el DLL de MAPI denominado [HrDispatchNotifications](hrdispatchnotifications.md) para que el procesamiento sea aún más sencillo.</span><span class="sxs-lookup"><span data-stu-id="310c3-110">Implementing the logic to achieve this can be done fairly simply, but MAPI provides an entry point into the MAPI DLL called [HrDispatchNotifications](hrdispatchnotifications.md) to make processing even simpler.</span></span> <span data-ttu-id="310c3-111">Llama **a HrDispatchNotifications** de la siguiente manera para recibir notificaciones en el cliente:</span><span class="sxs-lookup"><span data-stu-id="310c3-111">Call **HrDispatchNotifications** as follows to receive notifications in your client:</span></span> 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


