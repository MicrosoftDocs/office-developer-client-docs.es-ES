---
title: Enviar y recibir notificaciones de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4ee47b51a98cf732f4e9af2a87fa1734a7250208
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431858"
---
# <a name="sending-and-receiving-form-notifications"></a><span data-ttu-id="0a92d-103">Enviar y recibir notificaciones de formulario</span><span class="sxs-lookup"><span data-stu-id="0a92d-103">Sending and Receiving Form Notifications</span></span>

  
  
<span data-ttu-id="0a92d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a92d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a92d-105">Las notificaciones de formulario se usan en MAPI para facilitar la comunicación desde el formulario hasta el visor, así como desde el visor hasta el formulario.</span><span class="sxs-lookup"><span data-stu-id="0a92d-105">Form notifications are used in MAPI to facilitate communication both from the form to your viewer as well as from your viewer to the form.</span></span>
  
<span data-ttu-id="0a92d-106">Los formularios envían notificaciones al visor cuando se produce uno de los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="0a92d-106">Forms send notifications to your viewer when one of the following events occur:</span></span>
  
- <span data-ttu-id="0a92d-107">El formulario está cerrado.</span><span class="sxs-lookup"><span data-stu-id="0a92d-107">The form is closed.</span></span>
    
- <span data-ttu-id="0a92d-108">Se carga un nuevo mensaje en el formulario.</span><span class="sxs-lookup"><span data-stu-id="0a92d-108">A new message is loaded in the form.</span></span>
    
- <span data-ttu-id="0a92d-109">Se ha completado una operación de guardado.</span><span class="sxs-lookup"><span data-stu-id="0a92d-109">A save operation is completed.</span></span>
    
- <span data-ttu-id="0a92d-110">Se envía un mensaje.</span><span class="sxs-lookup"><span data-stu-id="0a92d-110">A message is sent.</span></span>
    
<span data-ttu-id="0a92d-111">Cada uno de estos tipos de evento corresponde a un método determinado en [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md), una de las interfaces que el visor de formularios debe implementar.</span><span class="sxs-lookup"><span data-stu-id="0a92d-111">Each of these event types correspond to a particular method in [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), one of the interfaces that your form viewer must implement.</span></span> <span data-ttu-id="0a92d-112">Cuando se produce un evento, el formulario llama al método **IMAPIViewAdviseSink** correspondiente en el receptor de notificaciones de su visor.</span><span class="sxs-lookup"><span data-stu-id="0a92d-112">When an event occurs, the form calls the corresponding **IMAPIViewAdviseSink** method in your viewer's advise sink.</span></span> <span data-ttu-id="0a92d-113">Por ejemplo, cuando llega un nuevo mensaje que el espectador debe incluir en la pantalla, el formulario llama al método [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="0a92d-113">For example, when a new message arrives that your viewer should include in its display, the form calls your [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) method.</span></span> 
  
<span data-ttu-id="0a92d-114">Implemente su vista notificar al receptor de un modo que tenga sentido para su visor; no hay una implementación estándar.</span><span class="sxs-lookup"><span data-stu-id="0a92d-114">Implement your view advise sink in a way that makes sense for your viewer; there is no standard implementation.</span></span> <span data-ttu-id="0a92d-115">Por ejemplo, en **OnNewMessage** , puede actualizar la vista de la tabla de contenido de la carpeta actual para incluir el mensaje recién llegado.</span><span class="sxs-lookup"><span data-stu-id="0a92d-115">For example, in **OnNewMessage** you can update the view of the current folder's contents table to include the newly arrived message.</span></span> <span data-ttu-id="0a92d-116">En [IMAPIViewAdviseSink::](imapiviewadvisesink-onsubmitted.md)alsent, el método al que se llama cuando recibe un evento de mensaje enviado, puede copiar el mensaje enviado a una carpeta de elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="0a92d-116">In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), the method that is called when you receive a submitted message event, you can copy the submitted message to a Sent Items folder.</span></span>
  
<span data-ttu-id="0a92d-117">Los formularios reciben una notificación del visor cuando se produce un cambio que afecta al formulario y al cargar un mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="0a92d-117">Forms receive notification from your viewer when a change occurs that affects the form and when you are loading a new message.</span></span> <span data-ttu-id="0a92d-118">Para notificar a un formulario, llame a uno de los métodos de **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink:: onchange](imapiformadvisesink-onchange.md) o [IMAPIFormAdviseSink:: OnActivateNext](imapiformadvisesink-onactivatenext.md).</span><span class="sxs-lookup"><span data-stu-id="0a92d-118">To notify a form, call one of the methods of **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) or [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span></span> <span data-ttu-id="0a92d-119">Llame a **onchange** para comunicar el estado.</span><span class="sxs-lookup"><span data-stu-id="0a92d-119">Call **OnChange** to communicate status.</span></span> <span data-ttu-id="0a92d-120">Por ejemplo, si el formulario muestra el último elemento de una carpeta cuando llega un nuevo mensaje, llame a **onchange** con la marca VCSTATUS_NEXT establecida para indicar al formulario que ahora hay un elemento siguiente.</span><span class="sxs-lookup"><span data-stu-id="0a92d-120">For example, if the form is displaying the last item in a folder when a new message arrives, call **OnChange** with the VCSTATUS_NEXT flag set to tell the form that there is now a next item.</span></span> 
  
<span data-ttu-id="0a92d-121">Llame a **OnActivateNext** para avisar al formulario de la llegada de un nuevo mensaje que puede o no puede mostrar.</span><span class="sxs-lookup"><span data-stu-id="0a92d-121">Call **OnActivateNext** to alert the form to the arrival of a new message that it may or may not be able to display.</span></span> <span data-ttu-id="0a92d-122">Pase la clase de mensaje del mensaje a **OnActivateNext**.</span><span class="sxs-lookup"><span data-stu-id="0a92d-122">Pass the message class of the message to **OnActivateNext**.</span></span> 
  
<span data-ttu-id="0a92d-123">Las notificaciones de un objeto de formulario a la aplicación cliente se controlan mediante la interfaz **IMAPIViewAdviseSink** de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="0a92d-123">Notifications by a form object to the client application are handled by the client application's **IMAPIViewAdviseSink** interface.</span></span> <span data-ttu-id="0a92d-124">Para obtener más información, vea [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="0a92d-124">For more information, see [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).</span></span>
  

