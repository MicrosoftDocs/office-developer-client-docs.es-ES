---
title: IMsgStore IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore
api_type:
- COM
ms.assetid: 20090114-b183-4767-8971-a304a9aa47e6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: af4bf73b58f7723066bb8fad7c087ba0238ceec2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422330"
---
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="dc069-103">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dc069-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="dc069-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc069-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc069-105">Proporciona acceso a la información del almacén de mensajes y a los mensajes y carpetas.</span><span class="sxs-lookup"><span data-stu-id="dc069-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc069-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="dc069-106">Header file:</span></span>  <br/> |<span data-ttu-id="dc069-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc069-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="dc069-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="dc069-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="dc069-109">Objeto de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="dc069-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="dc069-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="dc069-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="dc069-111">Proveedores de al almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="dc069-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="dc069-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="dc069-112">Called by:</span></span>  <br/> |<span data-ttu-id="dc069-113">Aplicaciones cliente, la cola MAPI y MAPI</span><span class="sxs-lookup"><span data-stu-id="dc069-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="dc069-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="dc069-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="dc069-115">IID_IMsgStore</span><span class="sxs-lookup"><span data-stu-id="dc069-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="dc069-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="dc069-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="dc069-117">LPMDB</span><span class="sxs-lookup"><span data-stu-id="dc069-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="dc069-118">Modelo de transacción:</span><span class="sxs-lookup"><span data-stu-id="dc069-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="dc069-119">Notransacted</span><span class="sxs-lookup"><span data-stu-id="dc069-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="dc069-120">Orden de tabla virtual</span><span class="sxs-lookup"><span data-stu-id="dc069-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="dc069-121">Aconsejar</span><span class="sxs-lookup"><span data-stu-id="dc069-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="dc069-122">Se registra para recibir una notificación de eventos especificados que afectan al almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="dc069-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="dc069-123">Unadvise</span><span class="sxs-lookup"><span data-stu-id="dc069-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="dc069-124">Cancela el envío de notificaciones previamente configuradas con una llamada al método **IMsgStore::Advise.**</span><span class="sxs-lookup"><span data-stu-id="dc069-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="dc069-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="dc069-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="dc069-126">Compara dos identificadores de entrada para determinar si hacen referencia a la misma entrada en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="dc069-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="dc069-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="dc069-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="dc069-128">Abre una carpeta o un mensaje y devuelve un puntero de interfaz para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="dc069-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="dc069-129">SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="dc069-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="dc069-130">Establece una carpeta como destino de los mensajes entrantes de una clase de mensaje determinada.</span><span class="sxs-lookup"><span data-stu-id="dc069-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="dc069-131">GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="dc069-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="dc069-132">Obtiene la carpeta que se estableció como destino para los mensajes entrantes de una clase de mensaje especificada o como la carpeta de recepción predeterminada para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="dc069-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="dc069-133">GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="dc069-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="dc069-134">Proporciona acceso a la tabla de carpetas de recepción, una tabla con información sobre todas las carpetas de recepción para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="dc069-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="dc069-135">StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="dc069-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="dc069-136">Habilita el cierre de sesión orden del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="dc069-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="dc069-137">AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="dc069-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="dc069-138">Intenta quitar un mensaje de la cola saliente.</span><span class="sxs-lookup"><span data-stu-id="dc069-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="dc069-139">GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="dc069-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="dc069-140">Proporciona acceso a la tabla de cola saliente, una tabla con información sobre todos los mensajes de la cola saliente del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="dc069-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="dc069-141">SetLockState</span><span class="sxs-lookup"><span data-stu-id="dc069-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="dc069-142">Bloquea o desbloquea un mensaje.</span><span class="sxs-lookup"><span data-stu-id="dc069-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="dc069-143">FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="dc069-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="dc069-144">Permite que el proveedor del almacén de mensajes realice el procesamiento en un mensaje enviado.</span><span class="sxs-lookup"><span data-stu-id="dc069-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="dc069-145">NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="dc069-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="dc069-146">Informa el almac�n de mensajes que ha llegado un mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="dc069-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="dc069-147">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="dc069-147">**Required properties**</span></span>|<span data-ttu-id="dc069-148">**Nivel de acceso**</span><span class="sxs-lookup"><span data-stu-id="dc069-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc069-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dc069-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dc069-150">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dc069-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="dc069-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dc069-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dc069-152">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc069-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="dc069-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dc069-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dc069-154">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc069-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="dc069-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dc069-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dc069-156">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc069-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="dc069-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dc069-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dc069-158">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc069-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="dc069-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dc069-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dc069-160">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc069-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="dc069-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dc069-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dc069-162">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc069-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="dc069-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dc069-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dc069-164">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc069-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="dc069-165">Las siguientes propiedades son para almacenes de mensajes de mensajes interpersonales (IPM):</span><span class="sxs-lookup"><span data-stu-id="dc069-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="dc069-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dc069-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="dc069-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dc069-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="dc069-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dc069-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="dc069-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dc069-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="dc069-170">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="dc069-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="dc069-171">**PR_STORE_SUPPORT_MASK**</span><span class="sxs-lookup"><span data-stu-id="dc069-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc069-172">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dc069-172">See also</span></span>



[<span data-ttu-id="dc069-173">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dc069-173">MAPI Properties</span></span>](mapi-properties.md)

