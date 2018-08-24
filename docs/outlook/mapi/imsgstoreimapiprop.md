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
ms.openlocfilehash: 4ed17fd7f826432da9460fe01e5aa76802726bad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584635"
---
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="bccc0-103">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bccc0-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="bccc0-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bccc0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bccc0-105">Proporciona acceso al almacén de información del mensaje y a los mensajes y carpetas.</span><span class="sxs-lookup"><span data-stu-id="bccc0-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bccc0-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="bccc0-106">Header file:</span></span>  <br/> |<span data-ttu-id="bccc0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bccc0-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="bccc0-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="bccc0-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="bccc0-109">Objeto de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="bccc0-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="bccc0-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="bccc0-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="bccc0-111">Proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="bccc0-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="bccc0-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="bccc0-112">Called by:</span></span>  <br/> |<span data-ttu-id="bccc0-113">Las aplicaciones cliente, la cola MAPI y MAPI</span><span class="sxs-lookup"><span data-stu-id="bccc0-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="bccc0-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="bccc0-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="bccc0-115">IID_IMsgStore</span><span class="sxs-lookup"><span data-stu-id="bccc0-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="bccc0-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="bccc0-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="bccc0-117">LPMDB</span><span class="sxs-lookup"><span data-stu-id="bccc0-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="bccc0-118">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="bccc0-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="bccc0-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="bccc0-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="bccc0-120">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="bccc0-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="bccc0-121">Aviso</span><span class="sxs-lookup"><span data-stu-id="bccc0-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="bccc0-122">Se registra para recibir notificaciones de los eventos que afectan el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bccc0-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="bccc0-123">Desaconsejar</span><span class="sxs-lookup"><span data-stu-id="bccc0-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="bccc0-124">Cancela el envío de notificaciones configuradas previamente con una llamada al método **IMsgStore::Advise** .</span><span class="sxs-lookup"><span data-stu-id="bccc0-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="bccc0-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="bccc0-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="bccc0-126">Compara dos identificadores de entrada para determinar si hacen referencia a la misma entrada en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bccc0-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="bccc0-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="bccc0-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="bccc0-128">Se abre una carpeta o un mensaje y devuelve un puntero de interfaz para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="bccc0-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="bccc0-129">SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="bccc0-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="bccc0-130">Establece una carpeta como destino de los mensajes entrantes de una clase de mensaje en particular.</span><span class="sxs-lookup"><span data-stu-id="bccc0-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="bccc0-131">GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="bccc0-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="bccc0-132">Obtiene la carpeta que se estableció como el destino para los mensajes entrantes de una clase de mensaje especificado o como el valor predeterminado de recepción carpeta para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bccc0-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="bccc0-133">GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="bccc0-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="bccc0-134">Proporciona acceso a la tabla de la carpeta de recepción, una tabla con información acerca de todas las carpetas de recepción para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bccc0-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="bccc0-135">StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="bccc0-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="bccc0-136">Permite el cierre de sesión ordenada del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bccc0-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="bccc0-137">AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="bccc0-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="bccc0-138">Intenta quitar un mensaje de la cola de salida.</span><span class="sxs-lookup"><span data-stu-id="bccc0-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="bccc0-139">GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="bccc0-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="bccc0-140">Proporciona acceso a la tabla de cola saliente, una tabla que contiene información acerca de todos los mensajes en cola de salida del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bccc0-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="bccc0-141">SetLockState</span><span class="sxs-lookup"><span data-stu-id="bccc0-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="bccc0-142">Bloquea o desbloquea un mensaje.</span><span class="sxs-lookup"><span data-stu-id="bccc0-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="bccc0-143">FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="bccc0-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="bccc0-144">Permite que el proveedor de almacén de mensajes realizar el procesamiento en un mensaje enviado.</span><span class="sxs-lookup"><span data-stu-id="bccc0-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="bccc0-145">NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="bccc0-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="bccc0-146">Informa el almac�n de mensajes que ha llegado un mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="bccc0-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="bccc0-147">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="bccc0-147">**Required properties**</span></span>|<span data-ttu-id="bccc0-148">**Nivel de acceso**</span><span class="sxs-lookup"><span data-stu-id="bccc0-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bccc0-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bccc0-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bccc0-150">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="bccc0-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="bccc0-151">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bccc0-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bccc0-152">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bccc0-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="bccc0-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bccc0-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bccc0-154">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bccc0-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="bccc0-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bccc0-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bccc0-156">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bccc0-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="bccc0-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bccc0-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bccc0-158">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bccc0-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="bccc0-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bccc0-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bccc0-160">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bccc0-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="bccc0-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bccc0-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bccc0-162">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bccc0-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="bccc0-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bccc0-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bccc0-164">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bccc0-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="bccc0-165">Las siguientes propiedades son para los almacenes de mensajes mensajes interpersonales (IPM):</span><span class="sxs-lookup"><span data-stu-id="bccc0-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="bccc0-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bccc0-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="bccc0-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bccc0-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="bccc0-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bccc0-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="bccc0-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bccc0-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="bccc0-170">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="bccc0-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="bccc0-171">**PR_STORE_SUPPORT_MASK**</span><span class="sxs-lookup"><span data-stu-id="bccc0-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bccc0-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="bccc0-172">See also</span></span>



[<span data-ttu-id="bccc0-173">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bccc0-173">MAPI Properties</span></span>](mapi-properties.md)

