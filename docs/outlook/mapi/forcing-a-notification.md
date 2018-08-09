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
ms.openlocfilehash: 40fc763071f7113e222c6987dfd70fb7d89bab4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816845"
---
# <a name="forcing-a-notification"></a><span data-ttu-id="a46cb-103">Forzar una notificación</span><span class="sxs-lookup"><span data-stu-id="a46cb-103">Forcing a Notification</span></span>

  
  
<span data-ttu-id="a46cb-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a46cb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a46cb-105">Uso de proveedores de servicio cuando la [IMAPISupport: IUnknown](imapisupportiunknown.md) métodos de notificación, MAPI ofrece las notificaciones mediante una ventana oculta y su correspondiente procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="a46cb-105">When service providers use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods for notification, MAPI delivers notifications using a hidden window and its corresponding window procedure.</span></span> <span data-ttu-id="a46cb-106">Para que cada proceso recibir una notificación, MAPI envía un mensaje especial a la ventana oculta.</span><span class="sxs-lookup"><span data-stu-id="a46cb-106">For each process to receive a notification, MAPI posts a special message to the hidden window.</span></span> <span data-ttu-id="a46cb-107">Este mensaje se denomina con la constante **szMAPINotificationMsg** que se define en MAPIDEFS. H.</span><span class="sxs-lookup"><span data-stu-id="a46cb-107">This message is named with the constant **szMAPINotificationMsg** which is defined in MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="a46cb-108">Recibir estas notificaciones cuando el procedimiento de la ventana de la ventana oculta procesa el mensaje **szMAPINotificationMsg** .</span><span class="sxs-lookup"><span data-stu-id="a46cb-108">You receive these notifications when the hidden window's window procedure processes the **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="a46cb-109">Para garantizar que las notificaciones se entregan, es necesario esperar para y enviar este mensaje **szMAPINotificationMsg** .</span><span class="sxs-lookup"><span data-stu-id="a46cb-109">To guarantee that notifications are delivered, it is necessary to wait for and dispatch this **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="a46cb-110">Implementar la lógica para realizar esta acción puede realizarse bastante simplemente, pero MAPI proporciona un punto de entrada a la DLL MAPI denominada [HrDispatchNotifications](hrdispatchnotifications.md) para hacer que el procesamiento aún más sencillo.</span><span class="sxs-lookup"><span data-stu-id="a46cb-110">Implementing the logic to achieve this can be done fairly simply, but MAPI provides an entry point into the MAPI DLL called [HrDispatchNotifications](hrdispatchnotifications.md) to make processing even simpler.</span></span> <span data-ttu-id="a46cb-111">Llamar a **HrDispatchNotifications** como se indica a continuación para recibir notificaciones en su cliente:</span><span class="sxs-lookup"><span data-stu-id="a46cb-111">Call **HrDispatchNotifications** as follows to receive notifications in your client:</span></span> 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


