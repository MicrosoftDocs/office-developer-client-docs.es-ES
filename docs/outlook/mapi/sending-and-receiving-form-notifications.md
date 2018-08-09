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
ms.openlocfilehash: 4730fb04d530fce516fe1ca4fd572c58fc1f1ffa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820614"
---
# <a name="sending-and-receiving-form-notifications"></a><span data-ttu-id="0ec98-103">Enviar y recibir notificaciones de formulario</span><span class="sxs-lookup"><span data-stu-id="0ec98-103">Sending and Receiving Form Notifications</span></span>

  
  
<span data-ttu-id="0ec98-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0ec98-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0ec98-105">Notificaciones de formulario se usan en MAPI para facilitar la comunicación tanto desde el formulario a su visor, así como desde el visor al formulario.</span><span class="sxs-lookup"><span data-stu-id="0ec98-105">Form notifications are used in MAPI to facilitate communication both from the form to your viewer as well as from your viewer to the form.</span></span>
  
<span data-ttu-id="0ec98-106">Formularios de envían notificaciones a su visor cuando se producen uno de los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="0ec98-106">Forms send notifications to your viewer when one of the following events occur:</span></span>
  
- <span data-ttu-id="0ec98-107">Se cierra el formulario.</span><span class="sxs-lookup"><span data-stu-id="0ec98-107">The form is closed.</span></span>
    
- <span data-ttu-id="0ec98-108">Se carga un nuevo mensaje en el formulario.</span><span class="sxs-lookup"><span data-stu-id="0ec98-108">A new message is loaded in the form.</span></span>
    
- <span data-ttu-id="0ec98-109">Se completa una operación de guardar.</span><span class="sxs-lookup"><span data-stu-id="0ec98-109">A save operation is completed.</span></span>
    
- <span data-ttu-id="0ec98-110">Se envía un mensaje.</span><span class="sxs-lookup"><span data-stu-id="0ec98-110">A message is sent.</span></span>
    
<span data-ttu-id="0ec98-111">Cada uno de estos tipos de evento corresponden a un método concreto en [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md), una de las interfaces que debe implementar el Visor de formulario.</span><span class="sxs-lookup"><span data-stu-id="0ec98-111">Each of these event types correspond to a particular method in [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), one of the interfaces that your form viewer must implement.</span></span> <span data-ttu-id="0ec98-112">Cuando se produce un evento, las llamadas de formulario **IMAPIViewAdviseSink** del método correspondiente en el Visor del aviso receptor.</span><span class="sxs-lookup"><span data-stu-id="0ec98-112">When an event occurs, the form calls the corresponding **IMAPIViewAdviseSink** method in your viewer's advise sink.</span></span> <span data-ttu-id="0ec98-113">Por ejemplo, cuando llega un nuevo mensaje que debe incluir el Visor en su presentación, el formulario llama al método [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="0ec98-113">For example, when a new message arrives that your viewer should include in its display, the form calls your [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) method.</span></span> 
  
<span data-ttu-id="0ec98-114">Implementar la vista de aviso receptor en una forma que tiene sentido para su Visor; No hay ninguna implementación estándar.</span><span class="sxs-lookup"><span data-stu-id="0ec98-114">Implement your view advise sink in a way that makes sense for your viewer; there is no standard implementation.</span></span> <span data-ttu-id="0ec98-115">Por ejemplo, puede actualizar la vista de tabla de contenido de la carpeta actual para incluir el mensaje recién llegado en **OnNewMessage** .</span><span class="sxs-lookup"><span data-stu-id="0ec98-115">For example, in **OnNewMessage** you can update the view of the current folder's contents table to include the newly arrived message.</span></span> <span data-ttu-id="0ec98-116">En [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), el método que se llama cuando se recibe un evento de mensaje enviado, puede copiar el mensaje enviado a una carpeta de elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="0ec98-116">In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), the method that is called when you receive a submitted message event, you can copy the submitted message to a Sent Items folder.</span></span>
  
<span data-ttu-id="0ec98-117">Formularios de reciben una notificación de su visor cuando se produce un cambio que influye en el formulario y cuando se carga un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="0ec98-117">Forms receive notification from your viewer when a change occurs that affects the form and when you are loading a new message.</span></span> <span data-ttu-id="0ec98-118">Para notificar a un formulario, llame a uno de los métodos de **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) o [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span><span class="sxs-lookup"><span data-stu-id="0ec98-118">To notify a form, call one of the methods of **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) or [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span></span> <span data-ttu-id="0ec98-119">Llamada **OnChange** para comunicar el estado.</span><span class="sxs-lookup"><span data-stu-id="0ec98-119">Call **OnChange** to communicate status.</span></span> <span data-ttu-id="0ec98-120">Por ejemplo, si el formulario muestra el último elemento en una carpeta cuando llegue un nuevo mensaje, llamada **OnChange** con el indicador VCSTATUS_NEXT establecido para indicar que el formulario que ahora es un elemento siguiente.</span><span class="sxs-lookup"><span data-stu-id="0ec98-120">For example, if the form is displaying the last item in a folder when a new message arrives, call **OnChange** with the VCSTATUS_NEXT flag set to tell the form that there is now a next item.</span></span> 
  
<span data-ttu-id="0ec98-121">Llame a **OnActivateNext** para el formulario a la llegada de un nuevo mensaje de alerta que pueden o no pueden ser capaz de mostrar.</span><span class="sxs-lookup"><span data-stu-id="0ec98-121">Call **OnActivateNext** to alert the form to the arrival of a new message that it may or may not be able to display.</span></span> <span data-ttu-id="0ec98-122">Pase la clase de mensaje del mensaje a **OnActivateNext**.</span><span class="sxs-lookup"><span data-stu-id="0ec98-122">Pass the message class of the message to **OnActivateNext**.</span></span> 
  
<span data-ttu-id="0ec98-123">Las notificaciones por un objeto de formulario a la aplicación cliente se controlan mediante la interfaz de **IMAPIViewAdviseSink** de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="0ec98-123">Notifications by a form object to the client application are handled by the client application's **IMAPIViewAdviseSink** interface.</span></span> <span data-ttu-id="0ec98-124">Para obtener más información, vea [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="0ec98-124">For more information, see [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).</span></span>
  

