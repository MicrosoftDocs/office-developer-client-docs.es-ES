---
title: Enviar un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 33bf6780979ee25739abf93d89744e1517363c63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820446"
---
# <a name="posting-a-message"></a><span data-ttu-id="e121d-103">Enviar un mensaje</span><span class="sxs-lookup"><span data-stu-id="e121d-103">Posting a message</span></span>

<span data-ttu-id="e121d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e121d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e121d-105">Enviar un mensaje es similar a enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="e121d-105">Posting a message is similar to sending a message.</span></span> <span data-ttu-id="e121d-106">La diferencia principal es el destino.</span><span class="sxs-lookup"><span data-stu-id="e121d-106">The main difference is the destination.</span></span> <span data-ttu-id="e121d-107">En lugar de que se dirige a uno o más destinatarios a través de uno o varios sistemas de mensajería, un mensaje expuesto permanece en una carpeta en el almacén de mensajes actual.</span><span class="sxs-lookup"><span data-stu-id="e121d-107">Rather than being directed to one or more recipients across one or more messaging systems, a posted message remains in a folder in the current message store.</span></span>
  
### <a name="to-post-a-message"></a><span data-ttu-id="e121d-108">Para publicar un mensaje</span><span class="sxs-lookup"><span data-stu-id="e121d-108">To post a message</span></span>
  
1. <span data-ttu-id="e121d-109">Abra la carpeta de destino mediante una llamada a [IMsgStore::OpenEntry](imsgstore-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="e121d-109">Open the destination folder by calling [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="e121d-110">Si la carpeta de destino es la Bandeja de entrada, busque el identificador de entrada que se pase a **OpenEntry** mediante una llamada a [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="e121d-110">If the destination folder is the Inbox, locate the entry identifier to pass to **OpenEntry** by calling [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
2. <span data-ttu-id="e121d-111">Llame a [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para crear el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e121d-111">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create the message.</span></span> 
    
3. <span data-ttu-id="e121d-112">Llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) del mensaje para establecer:</span><span class="sxs-lookup"><span data-stu-id="e121d-112">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set:</span></span> 
    
   - <span data-ttu-id="e121d-113">El indicador MSGFLAG_READ en la propiedad **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e121d-113">The MSGFLAG_READ flag in the **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="e121d-114">Las propiedades **PR_SENDER** .</span><span class="sxs-lookup"><span data-stu-id="e121d-114">The **PR_SENDER** properties.</span></span> 
    
   - <span data-ttu-id="e121d-115">Las propiedades **PR_SENT_REPRESENTING** .</span><span class="sxs-lookup"><span data-stu-id="e121d-115">The **PR_SENT_REPRESENTING** properties.</span></span> 
    
   - <span data-ttu-id="e121d-116">La propiedad **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e121d-116">The **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="e121d-117">El **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) o la propiedad de **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e121d-117">The **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="e121d-118">La propiedad **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e121d-118">The **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="e121d-119">La propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e121d-119">The **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="e121d-120">Las propiedades requeridas por la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e121d-120">Any properties required by the message class.</span></span>
    
4. <span data-ttu-id="e121d-121">Llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje para guardar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e121d-121">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the message.</span></span> 
    
5. <span data-ttu-id="e121d-122">Si es necesario, cree un archivo adjunto, establezca sus propiedades y vuelva a guardarla.</span><span class="sxs-lookup"><span data-stu-id="e121d-122">If necessary, create an attachment, set its properties, and save it.</span></span> <span data-ttu-id="e121d-123">Para obtener más información acerca de cómo agregar datos adjuntos a los mensajes, vea [crear un datos adjuntos del mensaje](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="e121d-123">For more information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="e121d-124">Llame a **IMessage::SaveChanges** para guardar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e121d-124">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="e121d-125">En este momento aparecerá en la tabla de contenido de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="e121d-125">At this point it will appear in the contents table of the destination folder.</span></span> 
    
<span data-ttu-id="e121d-126">Tenga en cuenta que no se crea una lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="e121d-126">Notice that you do not create a recipient list.</span></span> <span data-ttu-id="e121d-127">En su lugar, establecer varias propiedades que se establecen normalmente por un proveedor de transporte de un mensaje enviado.</span><span class="sxs-lookup"><span data-stu-id="e121d-127">Instead, you set several properties that are normally set by a transport provider for a sent message.</span></span> 
  
<span data-ttu-id="e121d-128">Si desea guardar un mensaje de forma intermitente antes de que se muestran en la tabla de contenido de la carpeta visible, créelo en su lugar en una carpeta oculta, como la carpeta raíz del subárbol IPM y, a continuación, moverlo a la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="e121d-128">If you want to save a message intermittently before having it appear in the contents table of the visible folder, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the target folder.</span></span> 
  

