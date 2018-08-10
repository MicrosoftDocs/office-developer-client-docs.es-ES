---
title: Guardar un mensaje en la Bandeja de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3c48ded73d924a400632a94feab65f7afca6e526
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820545"
---
# <a name="saving-a-message-in-the-inbox"></a><span data-ttu-id="aece1-103">Guardar un mensaje en la Bandeja de entrada</span><span class="sxs-lookup"><span data-stu-id="aece1-103">Saving a Message in the Inbox</span></span>

  
  
<span data-ttu-id="aece1-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aece1-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="aece1-105">**Para almacenar un mensaje en la Bandeja de entrada sin todos los destinatarios**</span><span class="sxs-lookup"><span data-stu-id="aece1-105">**To store a message in the Inbox without any recipients**</span></span>
  
1. <span data-ttu-id="aece1-106">Llame a [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para recuperar el identificador de entrada de la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="aece1-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="aece1-107">Llame a [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir la Bandeja de entrada y recuperar un puntero a ella.</span><span class="sxs-lookup"><span data-stu-id="aece1-107">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the Inbox and retrieve a pointer to it.</span></span> 
    
3. <span data-ttu-id="aece1-108">Llamar al método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la Bandeja de entrada para crear el mensaje.</span><span class="sxs-lookup"><span data-stu-id="aece1-108">Call the Inbox's [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create the message.</span></span> 
    
4. <span data-ttu-id="aece1-109">Llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) del mensaje para agregar la **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), o **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) y **PR_SUBJECT** ([ PidTagSubject](pidtagsubject-canonical-property.md)) propiedades.</span><span class="sxs-lookup"><span data-stu-id="aece1-109">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to add the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) and **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) properties.</span></span> 
    
5. <span data-ttu-id="aece1-110">Crear cada dato adjunto, establezca sus propiedades y vuelva a guardarla.</span><span class="sxs-lookup"><span data-stu-id="aece1-110">Create each attachment, set its properties, and save it.</span></span> <span data-ttu-id="aece1-111">Para obtener información detallada sobre cómo agregar datos adjuntos a los mensajes, vea [crear un datos adjuntos del mensaje](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="aece1-111">For detailed information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="aece1-112">Llame a **IMessage::SaveChanges** para guardar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="aece1-112">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="aece1-113">En este momento aparecerá en la tabla de contenido de la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="aece1-113">At this point it will appear in the contents table of the Inbox.</span></span> 
    
<span data-ttu-id="aece1-114">Si desea guardar un intermittantly de mensaje antes de que se muestran en la tabla de contenido de la Bandeja de entrada, créelo en su lugar en una carpeta oculta, como la carpeta raíz del subárbol IPM y, a continuación, moverlo a la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="aece1-114">If you want to save a message intermittantly before having it appear in the contents table of the Inbox, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the Inbox.</span></span> 
  
