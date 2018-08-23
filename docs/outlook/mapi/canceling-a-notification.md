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
ms.openlocfilehash: 50d1fb451cbfcd07f97c5b12a9c86c03a435faa6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564776"
---
# <a name="canceling-a-notification"></a><span data-ttu-id="0d236-103">Cancelar una notificación</span><span class="sxs-lookup"><span data-stu-id="0d236-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="0d236-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d236-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d236-105">Para cancelar una notificación, los clientes llaman (método) de un origen advise **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="0d236-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="0d236-106">Llamar a **Unadvise** es importante debido a que se hace que el proveedor de servicios liberar su referencia a su receptor de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="0d236-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="0d236-107">Como un proveedor de servicios mantiene una referencia a un receptor de notificaciones, puede seguir el receptor de notificaciones recibir las llamadas de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="0d236-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="0d236-108">De hecho, debido a la naturaleza asincrónica de notificación de eventos, los clientes se pueden notificar incluso después de llamar a una correcta **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="0d236-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="0d236-109">Los clientes deben poder controlar la recepción de notificaciones en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="0d236-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="0d236-110">Debido a que difieren de las implementaciones del proveedor de servicio, los clientes que no se llama a **Unadvise** para cancelar una notificación no pueden suponer nada sobre cuando un proveedor liberará a su referencia a su receptor de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="0d236-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="0d236-111">Algunos proveedores de servicios de liberar sus referencias para receptores con notificación cuando éstos liberan sus orígenes advise.</span><span class="sxs-lookup"><span data-stu-id="0d236-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="0d236-112">Algunos proveedores de servicios de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="0d236-112">Some service providers do not.</span></span> <span data-ttu-id="0d236-113">Como un proveedor de servicios mantiene una referencia a un receptor de notificaciones, puede seguir ese receptor de notificaciones recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="0d236-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

