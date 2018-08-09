---
title: Volver a enviar un mensaje no entregado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4fd0bf5a542e006ec743dbb7fe03d3331875c6d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820508"
---
# <a name="resending-an-undelivered-message"></a><span data-ttu-id="9e615-103">Volver a enviar un mensaje no entregado</span><span class="sxs-lookup"><span data-stu-id="9e615-103">Resending an undelivered message</span></span>
  
<span data-ttu-id="9e615-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9e615-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9e615-105">Un proveedor de transporte envía un informe de no entrega (NDR) cuando no puede entregar un mensaje que ha enviado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9e615-105">A transport provider sends a non-delivery report (NDR) when it cannot successfully deliver a message that you have submitted.</span></span> <span data-ttu-id="9e615-106">Es hasta el cliente si los usuarios pueden intentar volver a enviar estos mensajes no entregados.</span><span class="sxs-lookup"><span data-stu-id="9e615-106">It is up to the client whether or not users can attempt to resend these undelivered messages.</span></span> <span data-ttu-id="9e615-107">En caso de admitir volver a enviar mensajes, puede usar un formulario de MAPI o implementar el suyo propio.</span><span class="sxs-lookup"><span data-stu-id="9e615-107">If you support resending messages, you can either use a form provided by MAPI or implement your own.</span></span> <span data-ttu-id="9e615-108">El formulario MAPI muestra los nombres de los destinatarios con errores y el motivo del error de entrega, si es posible e incluye un botón que, cuando se selecciona, permite que un usuario a enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="9e615-108">The MAPI form displays the names of the failed recipients and the reason for the delivery failure, if possible, and includes a button that, when selected, allows a user to resend the message.</span></span>
  
<span data-ttu-id="9e615-109">Cuando se recibe un mensaje reciente, debe ser exactamente igual que el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="9e615-109">When a resent message is received, it should look exactly like the original message.</span></span> <span data-ttu-id="9e615-110">El destinatario debe ser no puede diferenciar entre un mensaje que se entregó en su primer intento de transmisión o un intento de subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="9e615-110">The recipient should be unable to differentiate between a message that was delivered on its first attempt at transmission or a subsequent attempt.</span></span> <span data-ttu-id="9e615-111">Las respuestas en este mensaje deberían funcionar exactamente como si el mensaje se había se ha enviado correctamente la primera vez.</span><span class="sxs-lookup"><span data-stu-id="9e615-111">Replies on this message should work exactly as if the message had been sent successfully the first time.</span></span>
  
### <a name="to-resend-an-undelivered-message"></a><span data-ttu-id="9e615-112">Volver a enviar un mensaje no entregado</span><span class="sxs-lookup"><span data-stu-id="9e615-112">To resend an undelivered message</span></span>
  
1. <span data-ttu-id="9e615-113">Llame a [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para crear un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="9e615-113">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create a new message.</span></span> 
    
2. <span data-ttu-id="9e615-114">Copiar todas las propiedades del mensaje original, excluyendo el ** PR_MESSAGE_RECIPIENTS ** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) (propiedad) y las propiedades **PR_SENDER** y **PR_SENT_REPRESENTING** .</span><span class="sxs-lookup"><span data-stu-id="9e615-114">Copy all of the properties from the original message, excluding the ** PR_MESSAGE_RECIPIENTS ** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property, and the **PR_SENDER** and **PR_SENT_REPRESENTING** properties.</span></span> <span data-ttu-id="9e615-115">Realice las modificaciones de propiedad siguientes:</span><span class="sxs-lookup"><span data-stu-id="9e615-115">Make the following property modifications:</span></span> 
    
   - <span data-ttu-id="9e615-116">Establezca **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) en el informe ** PR_ORIG_MESSAGE_CLASS ** ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) (propiedad).</span><span class="sxs-lookup"><span data-stu-id="9e615-116">Set **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) to the report's **PR_ORIG_MESSAGE_CLASS ** ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="9e615-117">Establecer la marca MSGFLAG_RESEND en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9e615-117">Set the MSGFLAG_RESEND flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="9e615-118">Establezca **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) en la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="9e615-118">Set **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) to the original message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="9e615-119">Para cada destinatario, establezca MAPI_SUBMITTED en la propiedad **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9e615-119">For each recipient, set MAPI_SUBMITTED in the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> 
    
   - <span data-ttu-id="9e615-120">Duplicar a cada destinatario con errores.</span><span class="sxs-lookup"><span data-stu-id="9e615-120">Duplicate each failed recipient.</span></span> <span data-ttu-id="9e615-121">Cambie la propiedad **PR_RECIPIENT_TYPE** para el destinatario duplicado a MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="9e615-121">Change the **PR_RECIPIENT_TYPE** property for the duplicated recipient to MAPI_P1.</span></span> <span data-ttu-id="9e615-122">Por lo tanto, para cada destinatario con errores hay ahora dos entradas en la tabla de destinatarios: una con **PR_RECIPIENT_TYPE** establecida en su valor original y la otra con **PR_RECIPIENT_TYPE** establecido en MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="9e615-122">Therefore, for each failed recipient there are now two entries in the recipient table: one with **PR_RECIPIENT_TYPE** set to its original value and the other with **PR_RECIPIENT_TYPE** set to MAPI_P1.</span></span> 
    
3. <span data-ttu-id="9e615-123">Llame a [ScCreateConversationIndex](sccreateconversationindex.md) para establecer una conversación de seguimiento si así lo desea.</span><span class="sxs-lookup"><span data-stu-id="9e615-123">Call [ScCreateConversationIndex](sccreateconversationindex.md) to set up conversation tracking if desired.</span></span> 
    
4. <span data-ttu-id="9e615-124">Llamar al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) del nuevo mensaje para actualizar la lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="9e615-124">Call the new message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to update the recipient list.</span></span> 
    
5. <span data-ttu-id="9e615-125">Llame a [IMessage::SubmitMessage](imessage-submitmessage.md) para guardar y enviar el mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="9e615-125">Call [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send the new message.</span></span> 
    

