---
title: Publicar un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2c174d48a19e23de725e1d5a1533130175f2ab00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350753"
---
# <a name="posting-a-message"></a><span data-ttu-id="9e7d1-103">Publicar un mensaje</span><span class="sxs-lookup"><span data-stu-id="9e7d1-103">Posting a message</span></span>

<span data-ttu-id="9e7d1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e7d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e7d1-105">La publicación de un mensaje es similar a enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="9e7d1-105">Posting a message is similar to sending a message.</span></span> <span data-ttu-id="9e7d1-106">La principal diferencia es el destino.</span><span class="sxs-lookup"><span data-stu-id="9e7d1-106">The main difference is the destination.</span></span> <span data-ttu-id="9e7d1-107">En lugar de dirigirse a uno o más destinatarios en uno o varios sistemas de mensajería, un mensaje publicado permanece en una carpeta del almacén de mensajes actual.</span><span class="sxs-lookup"><span data-stu-id="9e7d1-107">Rather than being directed to one or more recipients across one or more messaging systems, a posted message remains in a folder in the current message store.</span></span>
  
### <a name="to-post-a-message"></a><span data-ttu-id="9e7d1-108">Para publicar un mensaje</span><span class="sxs-lookup"><span data-stu-id="9e7d1-108">To post a message</span></span>
  
1. <span data-ttu-id="9e7d1-109">Para abrir la carpeta de destino, llame a [IMsgStore:: OpenEntry](imsgstore-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="9e7d1-109">Open the destination folder by calling [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="9e7d1-110">Si la carpeta de destino es la bandeja de entrada, busque el identificador de entrada que se va a pasar a **OpenEntry** llamando a [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="9e7d1-110">If the destination folder is the Inbox, locate the entry identifier to pass to **OpenEntry** by calling [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
2. <span data-ttu-id="9e7d1-111">Llame a [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) para crear el mensaje.</span><span class="sxs-lookup"><span data-stu-id="9e7d1-111">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create the message.</span></span> 
    
3. <span data-ttu-id="9e7d1-112">Llame al método [IMAPIProp:: SetProps](imapiprop-setprops.md) del mensaje para establecer:</span><span class="sxs-lookup"><span data-stu-id="9e7d1-112">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set:</span></span> 
    
   - <span data-ttu-id="9e7d1-113">La marca MSGFLAG_READ en la propiedad **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9e7d1-113">The MSGFLAG_READ flag in the **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="9e7d1-114">Las propiedades de **PR_SENDER** .</span><span class="sxs-lookup"><span data-stu-id="9e7d1-114">The **PR_SENDER** properties.</span></span> 
    
   - <span data-ttu-id="9e7d1-115">Las propiedades de **PR_SENT_REPRESENTING** .</span><span class="sxs-lookup"><span data-stu-id="9e7d1-115">The **PR_SENT_REPRESENTING** properties.</span></span> 
    
   - <span data-ttu-id="9e7d1-116">La propiedad **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9e7d1-116">The **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="9e7d1-117">Propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) o **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9e7d1-117">The **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="9e7d1-118">La propiedad **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9e7d1-118">The **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="9e7d1-119">La propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9e7d1-119">The **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="9e7d1-120">Las propiedades requeridas por la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="9e7d1-120">Any properties required by the message class.</span></span>
    
4. <span data-ttu-id="9e7d1-121">Llame al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) del mensaje para guardar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="9e7d1-121">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the message.</span></span> 
    
5. <span data-ttu-id="9e7d1-122">Si es necesario, cree un dato adjunto, establezca sus propiedades y guárdelo.</span><span class="sxs-lookup"><span data-stu-id="9e7d1-122">If necessary, create an attachment, set its properties, and save it.</span></span> <span data-ttu-id="9e7d1-123">Para obtener más información acerca de la adición de datos adjuntos a mensajes, consulte [Creating a Message Attachment](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="9e7d1-123">For more information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="9e7d1-124">Llame a **IMessage:: SaveChanges** para guardar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="9e7d1-124">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="9e7d1-125">En este momento, aparecerá en la tabla de contenido de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="9e7d1-125">At this point it will appear in the contents table of the destination folder.</span></span> 
    
<span data-ttu-id="9e7d1-126">Observe que no se crea una lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="9e7d1-126">Notice that you do not create a recipient list.</span></span> <span data-ttu-id="9e7d1-127">En su lugar, se establecen varias propiedades que normalmente establece un proveedor de transporte para un mensaje enviado.</span><span class="sxs-lookup"><span data-stu-id="9e7d1-127">Instead, you set several properties that are normally set by a transport provider for a sent message.</span></span> 
  
<span data-ttu-id="9e7d1-128">Si desea guardar un mensaje intermitentemente antes de que aparezca en la tabla de contenido de la carpeta visible, créelo en una carpeta oculta, como la carpeta raíz del subárbol IPM y, a continuación, muévalo a la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="9e7d1-128">If you want to save a message intermittently before having it appear in the contents table of the visible folder, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the target folder.</span></span> 
  

