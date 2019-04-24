---
title: Cancelar una notificación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fb0972638fdd062c99040694222724566281024f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326407"
---
# <a name="canceling-a-notification"></a><span data-ttu-id="5939d-103">Cancelar una notificación</span><span class="sxs-lookup"><span data-stu-id="5939d-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="5939d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5939d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5939d-105">Para cancelar una notificación, los clientes llaman al método desaconsejable de un origen de notificaciones. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5939d-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="5939d-106">Llamar \*\*\*\* a Unadvise es importante porque hace que el proveedor de servicios libere su referencia a su receptor de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="5939d-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="5939d-107">Siempre que un proveedor de servicios mantenga una referencia a un receptor de notificaciones, el receptor de notificaciones puede seguir recibiendo [IMAPIAdviseSink:: BENOTIFY](imapiadvisesink-onnotify.md) calls.</span><span class="sxs-lookup"><span data-stu-id="5939d-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="5939d-108">De hecho, debido a la naturaleza asincrónica de la notificación de eventos, se puede notificar a los clientes incluso \*\*\*\* después de una llamada de desaconsejar correctamente.</span><span class="sxs-lookup"><span data-stu-id="5939d-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="5939d-109">Los clientes deben poder administrar la recepción de notificaciones en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="5939d-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="5939d-110">Debido a que las implementaciones del proveedor de servicios son distintas \*\*\*\* , los clientes que no llaman a inaconsejable para cancelar una notificación no pueden asumir nada sobre cuándo un proveedor libera su referencia a su receptor de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="5939d-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="5939d-111">Algunos proveedores de servicios liberan sus referencias para informar a los receptores cuando liberan sus orígenes de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="5939d-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="5939d-112">Algunos proveedores de servicios no lo hacen.</span><span class="sxs-lookup"><span data-stu-id="5939d-112">Some service providers do not.</span></span> <span data-ttu-id="5939d-113">Siempre que un proveedor de servicios mantenga una referencia a un receptor de notificaciones, el receptor de notificaciones puede seguir recibiendo notificaciones.</span><span class="sxs-lookup"><span data-stu-id="5939d-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

