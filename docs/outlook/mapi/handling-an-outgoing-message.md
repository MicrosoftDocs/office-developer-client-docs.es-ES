---
title: Controlar los mensajes salientes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 07785ac82c41108b4333b3c370e3d2f5bfd1426a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407630"
---
# <a name="handling-an-outgoing-message"></a><span data-ttu-id="02360-103">Controlar los mensajes salientes</span><span class="sxs-lookup"><span data-stu-id="02360-103">Handling an outgoing message</span></span>

<span data-ttu-id="02360-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02360-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02360-105">Un mensaje saliente es un mensaje que se puede enviar a uno o más destinatarios a través de uno o más sistemas de mensajería o publicarse en una carpeta de un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="02360-105">An outgoing message is a message that can be sent to one or more recipients across one or more messaging systems or be posted to a folder in a message store.</span></span>
  
## <a name="create-and-send-an-outgoing-message"></a><span data-ttu-id="02360-106">Crear y enviar un mensaje saliente</span><span class="sxs-lookup"><span data-stu-id="02360-106">Create and send an outgoing message</span></span>
  
1. <span data-ttu-id="02360-107">Abra el almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="02360-107">Open the default message store.</span></span> <span data-ttu-id="02360-108">Para obtener más información, vea [Abrir un almacén de mensajes](opening-a-message-store.md) y Abrir el almacén de mensajes [predeterminado.](opening-the-default-message-store.md)</span><span class="sxs-lookup"><span data-stu-id="02360-108">For more information, see [Opening a Message Store](opening-a-message-store.md) and [Opening the Default Message Store](opening-the-default-message-store.md).</span></span>
    
2. <span data-ttu-id="02360-109">Abra la carpeta Bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="02360-109">Open the Outbox folder.</span></span> <span data-ttu-id="02360-110">Para obtener más información, vea [Abrir una carpeta de almacén de mensajes.](opening-a-message-store-folder.md)</span><span class="sxs-lookup"><span data-stu-id="02360-110">For more information, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
    
3. <span data-ttu-id="02360-111">Llame al método **IMAPIFolder::CreateMessage** de la carpeta Bandeja de salida para crear el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="02360-111">Call the Outbox folder's **IMAPIFolder::CreateMessage** method to create the new message.</span></span> <span data-ttu-id="02360-112">Para obtener más información, [vea IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span><span class="sxs-lookup"><span data-stu-id="02360-112">For more information, see [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span></span>
    
4. <span data-ttu-id="02360-113">Cree una lista de destinatarios con uno o más destinatarios resueltos.</span><span class="sxs-lookup"><span data-stu-id="02360-113">Create a recipient list with one or more resolved recipients.</span></span> <span data-ttu-id="02360-114">Para obtener más información, vea [Crear una lista de destinatarios.](creating-a-recipient-list.md)</span><span class="sxs-lookup"><span data-stu-id="02360-114">For more information, see [Creating a Recipient List](creating-a-recipient-list.md).</span></span>
    
5. <span data-ttu-id="02360-115">Opcionalmente, agregue un asunto.</span><span class="sxs-lookup"><span data-stu-id="02360-115">Optionally, add a subject.</span></span> <span data-ttu-id="02360-116">Para obtener más información, vea [Crear un asunto del mensaje.](creating-a-message-subject.md)</span><span class="sxs-lookup"><span data-stu-id="02360-116">For more information, see [Creating a Message Subject](creating-a-message-subject.md).</span></span>
    
6. <span data-ttu-id="02360-117">Agregue el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="02360-117">Add the message text.</span></span> <span data-ttu-id="02360-118">Para obtener más información, vea [Crear texto de mensaje.](creating-message-text.md)</span><span class="sxs-lookup"><span data-stu-id="02360-118">For more information, see [Creating Message Text](creating-message-text.md).</span></span>
    
7. <span data-ttu-id="02360-119">Si el texto del mensaje tiene formato, agregue información de representación.</span><span class="sxs-lookup"><span data-stu-id="02360-119">If the message text is formatted, add rendering information.</span></span> <span data-ttu-id="02360-120">Para obtener más información, vea [Agregar información de representación al texto con formato.](adding-rendering-information-to-formatted-text.md)</span><span class="sxs-lookup"><span data-stu-id="02360-120">For more information, see [Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md).</span></span>
    
8. <span data-ttu-id="02360-121">Opcionalmente, agregue uno o más datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="02360-121">Optionally, add one or more attachments.</span></span> <span data-ttu-id="02360-122">Para obtener más información, vea [Creación de datos adjuntos de un mensaje.](creating-a-message-attachment.md)</span><span class="sxs-lookup"><span data-stu-id="02360-122">For more information, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
9. <span data-ttu-id="02360-123">Establezca otras propiedades del mensaje como desee y, a continuación, guarde y envíe el mensaje llamando a **IMessage::SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="02360-123">Set other message properties as desired and then save and send the message by calling **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="02360-124">Para obtener más información, [vea IMessage::SubmitMessage](imessage-submitmessage.md).</span><span class="sxs-lookup"><span data-stu-id="02360-124">For more information, see [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span>
    
10. <span data-ttu-id="02360-125">Elimine el mensaje enviado si la propiedad **PR \_ DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) está establecida en TRUE o muévela a la carpeta identificada por la propiedad **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="02360-125">Delete the sent message if the **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property is set to TRUE or move it to the folder identified by the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="02360-126">Para obtener más información, vea [Procesamiento de un mensaje enviado.](processing-a-sent-message.md)</span><span class="sxs-lookup"><span data-stu-id="02360-126">For more information, see [Processing a Sent Message](processing-a-sent-message.md).</span></span>
    
<span data-ttu-id="02360-127">Si desea guardar el mensaje de forma intermitente antes de enviarlo, llame al método [IMAPIProp::SaveChanges del](imapiprop-savechanges.md) mensaje.</span><span class="sxs-lookup"><span data-stu-id="02360-127">If you want to intermittantly save the message before sending it, call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="02360-128">Para obtener más información, vea Guardar [un mensaje](saving-a-message.md) o Enviar [un mensaje.](sending-a-message.md)</span><span class="sxs-lookup"><span data-stu-id="02360-128">For more information, see, [Saving a Message](saving-a-message.md) or [Sending a Message](sending-a-message.md).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="02360-129">En esta sección</span><span class="sxs-lookup"><span data-stu-id="02360-129">In this section</span></span>

- <span data-ttu-id="02360-130">[Creación de una lista de destinatarios:](creating-a-recipient-list.md)describe cómo crear una lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="02360-130">[Creating a Recipient List](creating-a-recipient-list.md): Describes how to create a recipient list.</span></span>
    
- <span data-ttu-id="02360-131">[Creación de un asunto de](creating-a-message-subject.md)mensaje: describe cómo crear un asunto opcional para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="02360-131">[Creating a Message Subject](creating-a-message-subject.md): Describes how to create an optional subject for a message.</span></span>
    
- <span data-ttu-id="02360-132">[Creación de texto de](creating-message-text.md)mensaje: describe cómo crear texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="02360-132">[Creating Message Text](creating-message-text.md): Describes how to create message text.</span></span>
    
- <span data-ttu-id="02360-133">[Agregar información de representación al texto con](adding-rendering-information-to-formatted-text.md)formato: describe dónde se representarán los datos adjuntos en el texto con formato.</span><span class="sxs-lookup"><span data-stu-id="02360-133">[Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md): Describes where in formatted text an attachment is to be rendered.</span></span>
    
- <span data-ttu-id="02360-134">[Creación de datos adjuntos de](creating-a-message-attachment.md)mensajes: describe cómo crear datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="02360-134">[Creating a Message Attachment](creating-a-message-attachment.md): Describes how to create attachments.</span></span>
    
- <span data-ttu-id="02360-135">[Guardar un mensaje:](saving-a-message.md)describe cómo los clientes guardarán los mensajes.</span><span class="sxs-lookup"><span data-stu-id="02360-135">[Saving a Message](saving-a-message.md): Describes how clients save messages.</span></span>
    
- <span data-ttu-id="02360-136">[Enviar un mensaje:](sending-a-message.md)describe cómo enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="02360-136">[Sending a Message](sending-a-message.md): Describes how to send a message.</span></span>
    
- <span data-ttu-id="02360-137">[Procesamiento de un mensaje enviado:](processing-a-sent-message.md)describe cómo se pueden procesar los mensajes enviados.</span><span class="sxs-lookup"><span data-stu-id="02360-137">[Processing a Sent Message](processing-a-sent-message.md): Describes how to sent messages can be processed.</span></span>
    

