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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409765"
---
# <a name="canceling-a-notification"></a><span data-ttu-id="2adf7-103">Cancelar una notificación</span><span class="sxs-lookup"><span data-stu-id="2adf7-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="2adf7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2adf7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2adf7-105">Para cancelar una notificación, los clientes llaman al método **Unadvise** de un origen de aviso.</span><span class="sxs-lookup"><span data-stu-id="2adf7-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="2adf7-106">Llamar **a Unadvise** es importante porque hace que el proveedor de servicios libere su referencia al receptor de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="2adf7-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="2adf7-107">Siempre que un proveedor de servicios mantenga una referencia a un receptor de avisos, el receptor de notificaciones puede seguir recibiendo llamadas [IMAPIAdviseSink::OnNotify.](imapiadvisesink-onnotify.md)</span><span class="sxs-lookup"><span data-stu-id="2adf7-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="2adf7-108">De hecho, debido a la naturaleza asincrónica de la notificación de eventos, se puede notificar a los clientes incluso después de una llamada **unadvise** correcta.</span><span class="sxs-lookup"><span data-stu-id="2adf7-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="2adf7-109">Los clientes deben poder controlar la recepción de notificaciones en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="2adf7-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="2adf7-110">Dado que las implementaciones del proveedor de servicios difieren, los clientes que no pueden llamar a **Unadvise** para cancelar una notificación no pueden asumir nada acerca de cuándo un proveedor liberará su referencia al receptor de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="2adf7-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="2adf7-111">Algunos proveedores de servicios liberan sus referencias para avisar a los receptores cuando liberan sus orígenes de asesoramiento.</span><span class="sxs-lookup"><span data-stu-id="2adf7-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="2adf7-112">Algunos proveedores de servicios no lo hacen.</span><span class="sxs-lookup"><span data-stu-id="2adf7-112">Some service providers do not.</span></span> <span data-ttu-id="2adf7-113">Siempre que un proveedor de servicios mantenga una referencia a un receptor de notificaciones, ese receptor de avisos puede seguir recibiendo notificaciones.</span><span class="sxs-lookup"><span data-stu-id="2adf7-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

