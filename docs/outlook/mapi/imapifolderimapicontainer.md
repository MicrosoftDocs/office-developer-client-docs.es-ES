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
ms.openlocfilehash: 64a64029c3507d9ac4b520076a44e23170dd9bd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817262"
---
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="4a477-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="4a477-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="4a477-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a477-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a477-105">Realiza operaciones en los mensajes y subcarpetas en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4a477-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a477-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4a477-106">Header file:</span></span>  <br/> |<span data-ttu-id="4a477-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a477-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4a477-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="4a477-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="4a477-109">Objetos de carpeta</span><span class="sxs-lookup"><span data-stu-id="4a477-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="4a477-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="4a477-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="4a477-111">Proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="4a477-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="4a477-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="4a477-112">Called by:</span></span>  <br/> |<span data-ttu-id="4a477-113">Las aplicaciones cliente y MAPI</span><span class="sxs-lookup"><span data-stu-id="4a477-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="4a477-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="4a477-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4a477-115">IID_IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="4a477-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="4a477-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="4a477-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="4a477-117">LPMAPIFOLDER</span><span class="sxs-lookup"><span data-stu-id="4a477-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="4a477-118">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="4a477-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="4a477-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="4a477-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4a477-120">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="4a477-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4a477-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="4a477-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="4a477-122">Crea un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="4a477-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="4a477-123">CopyMessages</span><span class="sxs-lookup"><span data-stu-id="4a477-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="4a477-124">Copia o mueve uno o más mensajes.</span><span class="sxs-lookup"><span data-stu-id="4a477-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="4a477-125">DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="4a477-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="4a477-126">Elimina uno o más mensajes.</span><span class="sxs-lookup"><span data-stu-id="4a477-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="4a477-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="4a477-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="4a477-128">Crea una nueva subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="4a477-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="4a477-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="4a477-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="4a477-130">Copia o mueve una subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="4a477-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="4a477-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="4a477-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="4a477-132">Elimina una subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="4a477-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="4a477-133">SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="4a477-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="4a477-134">Establece o borra el indicador MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uno o varios de los mensajes de la carpeta y administra el envío de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="4a477-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="4a477-135">GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="4a477-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="4a477-136">Obtiene el estado asociado a un mensaje de una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="4a477-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="4a477-137">SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="4a477-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="4a477-138">Establece el estado asociado a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="4a477-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="4a477-139">SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="4a477-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="4a477-140">Establece el criterio de ordenación predeterminado para la tabla de contenido de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4a477-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="4a477-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="4a477-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="4a477-142">Elimina todos los mensajes y subcarpetas de una carpeta sin eliminar la propia carpeta.</span><span class="sxs-lookup"><span data-stu-id="4a477-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="4a477-143">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="4a477-143">**Required properties**</span></span>|<span data-ttu-id="4a477-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="4a477-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4a477-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4a477-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4a477-146">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4a477-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="4a477-147">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4a477-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4a477-148">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4a477-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="4a477-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4a477-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4a477-150">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4a477-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="4a477-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4a477-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4a477-152">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4a477-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="4a477-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4a477-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4a477-154">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4a477-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="4a477-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4a477-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4a477-156">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4a477-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="4a477-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4a477-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4a477-158">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4a477-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="4a477-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4a477-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4a477-160">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4a477-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4a477-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a477-161">See also</span></span>



[<span data-ttu-id="4a477-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="4a477-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

