---
title: Reenviar un mensaje sin entregar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ddd0c1419531b0822bb98df51f47e12e63dcf242
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432670"
---
# <a name="resending-an-undelivered-message"></a><span data-ttu-id="aed45-103">Reenviar un mensaje sin entregar</span><span class="sxs-lookup"><span data-stu-id="aed45-103">Resending an undelivered message</span></span>
  
<span data-ttu-id="aed45-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aed45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aed45-105">Un proveedor de transporte envía un informe de no entrega (NDR) cuando no puede entregar correctamente un mensaje que ha enviado.</span><span class="sxs-lookup"><span data-stu-id="aed45-105">A transport provider sends a non-delivery report (NDR) when it cannot successfully deliver a message that you have submitted.</span></span> <span data-ttu-id="aed45-106">El cliente puede decidir si los usuarios pueden intentar volver a enviar estos mensajes no entregados.</span><span class="sxs-lookup"><span data-stu-id="aed45-106">It is up to the client whether or not users can attempt to resend these undelivered messages.</span></span> <span data-ttu-id="aed45-107">Si admite reenviar mensajes, puede usar un formulario proporcionado por MAPI o implementar el suyo propio.</span><span class="sxs-lookup"><span data-stu-id="aed45-107">If you support resending messages, you can either use a form provided by MAPI or implement your own.</span></span> <span data-ttu-id="aed45-108">El formulario MAPI muestra los nombres de los destinatarios con errores y el motivo del error de entrega, si es posible, e incluye un botón que, cuando se selecciona, permite que un usuario vuelva a enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="aed45-108">The MAPI form displays the names of the failed recipients and the reason for the delivery failure, if possible, and includes a button that, when selected, allows a user to resend the message.</span></span>
  
<span data-ttu-id="aed45-109">Cuando se recibe un mensaje de reenviado, debe ser exactamente igual que el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="aed45-109">When a resent message is received, it should look exactly like the original message.</span></span> <span data-ttu-id="aed45-110">El destinatario no debe poder diferenciar entre un mensaje que se entregó en su primer intento de transmisión o en un intento posterior.</span><span class="sxs-lookup"><span data-stu-id="aed45-110">The recipient should be unable to differentiate between a message that was delivered on its first attempt at transmission or a subsequent attempt.</span></span> <span data-ttu-id="aed45-111">Las respuestas de este mensaje deben funcionar exactamente como si el mensaje se hubiera enviado correctamente la primera vez.</span><span class="sxs-lookup"><span data-stu-id="aed45-111">Replies on this message should work exactly as if the message had been sent successfully the first time.</span></span>
  
### <a name="to-resend-an-undelivered-message"></a><span data-ttu-id="aed45-112">Para volver a enviar un mensaje no entregado</span><span class="sxs-lookup"><span data-stu-id="aed45-112">To resend an undelivered message</span></span>
  
1. <span data-ttu-id="aed45-113">Llame [a IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para crear un mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="aed45-113">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create a new message.</span></span> 
    
2. <span data-ttu-id="aed45-114">Copie todas las propiedades del mensaje original, excepto la propiedad \*\* PR_MESSAGE_RECIPIENTS \*\* ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) y las propiedades **PR_SENDER** y **PR_SENT_REPRESENTING.**</span><span class="sxs-lookup"><span data-stu-id="aed45-114">Copy all of the properties from the original message, excluding the \*\* PR_MESSAGE_RECIPIENTS \*\* ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property, and the **PR_SENDER** and **PR_SENT_REPRESENTING** properties.</span></span> <span data-ttu-id="aed45-115">Realice las siguientes modificaciones de propiedad:</span><span class="sxs-lookup"><span data-stu-id="aed45-115">Make the following property modifications:</span></span> 
    
   - <span data-ttu-id="aed45-116">Establezca **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) en la propiedad \*\*PR_ORIG_MESSAGE_CLASS \*\* ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) del informe.</span><span class="sxs-lookup"><span data-stu-id="aed45-116">Set **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) to the report's \*\*PR_ORIG_MESSAGE_CLASS \*\* ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="aed45-117">Establezca la marca MSGFLAG_RESEND en la **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aed45-117">Set the MSGFLAG_RESEND flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="aed45-118">Establezca **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) en la propiedad PR_ENTRYID **del** mensaje original ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aed45-118">Set **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) to the original message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="aed45-119">Para cada destinatario, establezca MAPI_SUBMITTED en **la PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aed45-119">For each recipient, set MAPI_SUBMITTED in the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> 
    
   - <span data-ttu-id="aed45-120">Duplicar cada destinatario con errores.</span><span class="sxs-lookup"><span data-stu-id="aed45-120">Duplicate each failed recipient.</span></span> <span data-ttu-id="aed45-121">Cambie la **PR_RECIPIENT_TYPE** propiedad del destinatario duplicado a MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="aed45-121">Change the **PR_RECIPIENT_TYPE** property for the duplicated recipient to MAPI_P1.</span></span> <span data-ttu-id="aed45-122">Por lo tanto, para cada destinatario con error ahora hay dos entradas en la tabla de destinatarios: una con **PR_RECIPIENT_TYPE** establecido en su valor original y la otra con **PR_RECIPIENT_TYPE** establecido en MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="aed45-122">Therefore, for each failed recipient there are now two entries in the recipient table: one with **PR_RECIPIENT_TYPE** set to its original value and the other with **PR_RECIPIENT_TYPE** set to MAPI_P1.</span></span> 
    
3. <span data-ttu-id="aed45-123">Llama [a ScCreateConversationIndex para](sccreateconversationindex.md) configurar el seguimiento de conversaciones si lo deseas.</span><span class="sxs-lookup"><span data-stu-id="aed45-123">Call [ScCreateConversationIndex](sccreateconversationindex.md) to set up conversation tracking if desired.</span></span> 
    
4. <span data-ttu-id="aed45-124">Llame al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) del nuevo mensaje para actualizar la lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="aed45-124">Call the new message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to update the recipient list.</span></span> 
    
5. <span data-ttu-id="aed45-125">Llama [a IMessage::SubmitMessage](imessage-submitmessage.md) para guardar y enviar el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="aed45-125">Call [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send the new message.</span></span> 
    

