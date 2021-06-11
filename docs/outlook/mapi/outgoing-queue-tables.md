---
title: Tablas de cola salientes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4bf935f58fb20460bbf6baf4b1434be1f3ab8156
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437577"
---
# <a name="outgoing-queue-tables"></a><span data-ttu-id="29d45-103">Tablas de cola salientes</span><span class="sxs-lookup"><span data-stu-id="29d45-103">Outgoing Queue Tables</span></span>

  
  
<span data-ttu-id="29d45-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29d45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29d45-105">Una tabla de cola saliente contiene información sobre todos los mensajes salientes de un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="29d45-105">An outgoing queue table contains information about all the outgoing messages for a message store.</span></span> <span data-ttu-id="29d45-106">Los proveedores de almacén de mensajes implementan tablas de cola salientes para que la cola MAPI la use.</span><span class="sxs-lookup"><span data-stu-id="29d45-106">Message store providers implement outgoing queue tables for the MAPI spooler to use.</span></span> <span data-ttu-id="29d45-107">Los almacenes que no admiten el envío o la recepción de mensajes no necesitan implementar esta tabla.</span><span class="sxs-lookup"><span data-stu-id="29d45-107">Stores that do not support the sending or receiving of messages need not implement this table.</span></span> 
  
<span data-ttu-id="29d45-108">Para obtener acceso a una tabla de cola saliente, la cola MAPI llama al [método IMsgStore::GetOutgoingQueue.](imsgstore-getoutgoingqueue.md)</span><span class="sxs-lookup"><span data-stu-id="29d45-108">To access an outgoing queue table, the MAPI spooler calls the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method.</span></span> 
  
<span data-ttu-id="29d45-109">Existe el requisito de que los mensajes se preprocesan y se envíen al proveedor de transporte en el mismo orden en que se enviaron por la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="29d45-109">There is a requirement that messages be preprocessed and submitted to the transport provider in the same order as they were sent by the client application.</span></span> <span data-ttu-id="29d45-110">La cola MAPI está diseñada para aceptar mensajes del almacén de mensajes en orden ascendente de tiempo de envío.</span><span class="sxs-lookup"><span data-stu-id="29d45-110">The MAPI spooler is designed to accept messages from the message store in ascending order of submission time.</span></span> <span data-ttu-id="29d45-111">Debido a este requisito, puede haber algún retraso antes de que algunos mensajes aparezcan en la tabla de cola saliente.</span><span class="sxs-lookup"><span data-stu-id="29d45-111">Because of this requirement, there can be some delay before some messages appear in the outgoing queue table.</span></span> 
  
<span data-ttu-id="29d45-112">Los almacenes de mensajes deben permitir la ordenación en la tabla de cola saliente para que la cola MAPI pueda ordenar los mensajes por tiempo de envío, o bien el criterio de ordenación predeterminado debe ser por tiempo de envío ascendente.</span><span class="sxs-lookup"><span data-stu-id="29d45-112">Message stores should either allow sorting on the outgoing queue table so that the MAPI spooler can sort the messages by submission time, or the default sort order should be by ascending submission time.</span></span> 
  
<span data-ttu-id="29d45-113">La tabla de cola saliente debe enviar notificaciones cuando cambie el contenido de la cola.</span><span class="sxs-lookup"><span data-stu-id="29d45-113">The outgoing queue table must send notifications when the contents of the queue changes.</span></span>
  
<span data-ttu-id="29d45-114">Las siguientes propiedades son la columna necesaria establecida en las tablas de colas salientes:</span><span class="sxs-lookup"><span data-stu-id="29d45-114">The following properties make up the required column set in outgoing queue tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="29d45-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="29d45-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="29d45-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="29d45-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="29d45-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="29d45-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="29d45-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="29d45-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="29d45-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="29d45-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="29d45-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="29d45-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="29d45-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="29d45-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="29d45-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="29d45-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="29d45-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="29d45-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="29d45-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="29d45-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="29d45-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="29d45-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span></span>  <br/> | <br/> |
   
<span data-ttu-id="29d45-126">Para obtener más información acerca de cómo se usa la tabla de cola saliente, vea [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="29d45-126">For more information about how the outgoing queue table is used, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="29d45-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="29d45-127">See also</span></span>



[<span data-ttu-id="29d45-128">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="29d45-128">MAPI Tables</span></span>](mapi-tables.md)

