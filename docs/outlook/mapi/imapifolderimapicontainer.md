---
title: IMAPIFolder IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder
api_type:
- COM
ms.assetid: bc2e8d17-7687-43c2-8f01-b677703f7288
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5e31896354141999e02f2cba117ef9739340be61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424241"
---
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="0f362-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="0f362-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="0f362-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f362-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f362-105">Realiza operaciones en los mensajes y subcarpetas de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="0f362-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0f362-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0f362-106">Header file:</span></span>  <br/> |<span data-ttu-id="0f362-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f362-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0f362-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="0f362-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="0f362-109">Objetos Folder</span><span class="sxs-lookup"><span data-stu-id="0f362-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="0f362-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="0f362-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="0f362-111">Proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="0f362-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="0f362-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="0f362-112">Called by:</span></span>  <br/> |<span data-ttu-id="0f362-113">Aplicaciones cliente y MAPI</span><span class="sxs-lookup"><span data-stu-id="0f362-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="0f362-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="0f362-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0f362-115">IID_IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="0f362-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="0f362-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="0f362-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="0f362-117">LPMAPIFOLDER</span><span class="sxs-lookup"><span data-stu-id="0f362-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="0f362-118">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="0f362-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="0f362-119">No transacted</span><span class="sxs-lookup"><span data-stu-id="0f362-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0f362-120">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="0f362-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0f362-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="0f362-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="0f362-122">Crea un mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="0f362-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="0f362-123">CopyMessages</span><span class="sxs-lookup"><span data-stu-id="0f362-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="0f362-124">Copia o mueve uno o varios mensajes.</span><span class="sxs-lookup"><span data-stu-id="0f362-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="0f362-125">DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="0f362-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="0f362-126">Elimina uno o varios mensajes.</span><span class="sxs-lookup"><span data-stu-id="0f362-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="0f362-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="0f362-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="0f362-128">Crea una subcarpeta nueva.</span><span class="sxs-lookup"><span data-stu-id="0f362-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="0f362-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="0f362-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="0f362-130">Copia o mueve una subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="0f362-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="0f362-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="0f362-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="0f362-132">Elimina una subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="0f362-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="0f362-133">SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="0f362-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="0f362-134">Establece o borra la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uno o varios de los mensajes de la carpeta y administra el envío de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="0f362-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="0f362-135">GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="0f362-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="0f362-136">Obtiene el estado asociado a un mensaje en una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="0f362-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="0f362-137">SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="0f362-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="0f362-138">Establece el estado asociado a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="0f362-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="0f362-139">SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="0f362-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="0f362-140">Establece el criterio de ordenación predeterminado para la tabla de contenido de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="0f362-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="0f362-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="0f362-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="0f362-142">Elimina todos los mensajes y subcarpetas de una carpeta sin eliminar la carpeta en sí.</span><span class="sxs-lookup"><span data-stu-id="0f362-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="0f362-143">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="0f362-143">**Required properties**</span></span>|<span data-ttu-id="0f362-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="0f362-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0f362-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f362-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f362-146">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0f362-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="0f362-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f362-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f362-148">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f362-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="0f362-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f362-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f362-150">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0f362-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="0f362-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f362-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f362-152">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f362-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="0f362-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f362-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f362-154">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f362-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="0f362-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f362-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f362-156">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f362-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="0f362-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f362-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f362-158">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f362-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="0f362-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f362-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f362-160">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f362-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0f362-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f362-161">See also</span></span>



[<span data-ttu-id="0f362-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="0f362-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

