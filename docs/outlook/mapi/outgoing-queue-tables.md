---
title: Tablas de cola saliente
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c5f136a0d26b7519bc1b7b3d8f448f5f382767ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591257"
---
# <a name="outgoing-queue-tables"></a><span data-ttu-id="82a5a-103">Tablas de cola saliente</span><span class="sxs-lookup"><span data-stu-id="82a5a-103">Outgoing Queue Tables</span></span>

  
  
<span data-ttu-id="82a5a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82a5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82a5a-105">Una tabla de cola saliente contiene información sobre todos los mensajes salientes para un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="82a5a-105">An outgoing queue table contains information about all the outgoing messages for a message store.</span></span> <span data-ttu-id="82a5a-106">Los proveedores de almacén de mensajes implementan tablas de cola saliente para la cola MAPI usar.</span><span class="sxs-lookup"><span data-stu-id="82a5a-106">Message store providers implement outgoing queue tables for the MAPI spooler to use.</span></span> <span data-ttu-id="82a5a-107">Almacenes que no admiten el envío o recepción de mensajes, no necesita implementar esta tabla.</span><span class="sxs-lookup"><span data-stu-id="82a5a-107">Stores that do not support the sending or receiving of messages need not implement this table.</span></span> 
  
<span data-ttu-id="82a5a-108">Para obtener acceso a una tabla de cola saliente, la cola MAPI llama al método de [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) .</span><span class="sxs-lookup"><span data-stu-id="82a5a-108">To access an outgoing queue table, the MAPI spooler calls the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method.</span></span> 
  
<span data-ttu-id="82a5a-109">Hay un requisito que los mensajes se preprocesan y se envía al proveedor de transporte en el mismo orden tal y como se enviaron por la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="82a5a-109">There is a requirement that messages be preprocessed and submitted to the transport provider in the same order as they were sent by the client application.</span></span> <span data-ttu-id="82a5a-110">La cola MAPI está diseñada para aceptar los mensajes desde el almacén de mensajes en orden ascendente de tiempo de envío.</span><span class="sxs-lookup"><span data-stu-id="82a5a-110">The MAPI spooler is designed to accept messages from the message store in ascending order of submission time.</span></span> <span data-ttu-id="82a5a-111">Debido a este requisito, puede haber algunas retraso antes de que algunos mensajes aparecen en la tabla cola saliente.</span><span class="sxs-lookup"><span data-stu-id="82a5a-111">Because of this requirement, there can be some delay before some messages appear in the outgoing queue table.</span></span> 
  
<span data-ttu-id="82a5a-112">Almacenes de mensaje ya sea deben permitir que la ordenación en la tabla cola saliente de modo que la cola MAPI puede ordenar los mensajes por hora de envío, o el criterio de ordenación predeterminado debería estar por orden ascendente de tiempo de envío.</span><span class="sxs-lookup"><span data-stu-id="82a5a-112">Message stores should either allow sorting on the outgoing queue table so that the MAPI spooler can sort the messages by submission time, or the default sort order should be by ascending submission time.</span></span> 
  
<span data-ttu-id="82a5a-113">En la tabla cola saliente debe enviar notificaciones cuando cambia el contenido de la cola.</span><span class="sxs-lookup"><span data-stu-id="82a5a-113">The outgoing queue table must send notifications when the contents of the queue changes.</span></span>
  
<span data-ttu-id="82a5a-114">Las siguientes propiedades que conforman la columna requiere establecer en las tablas de cola saliente:</span><span class="sxs-lookup"><span data-stu-id="82a5a-114">The following properties make up the required column set in outgoing queue tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="82a5a-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a5a-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="82a5a-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a5a-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="82a5a-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a5a-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="82a5a-118">**PR_DISPLAY_TO de MAPI** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a5a-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="82a5a-119">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a5a-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="82a5a-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a5a-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="82a5a-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a5a-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="82a5a-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a5a-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="82a5a-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a5a-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="82a5a-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a5a-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="82a5a-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a5a-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span></span>  <br/> | <br/> |
   
<span data-ttu-id="82a5a-126">Para obtener más información acerca de cómo se usa la tabla de cola saliente, vea [Enviar mensajes mediante el uso de los proveedores de almacén de mensajes](sending-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="82a5a-126">For more information about how the outgoing queue table is used, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="82a5a-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="82a5a-127">See also</span></span>



[<span data-ttu-id="82a5a-128">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="82a5a-128">MAPI Tables</span></span>](mapi-tables.md)

