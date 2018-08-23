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
ms.openlocfilehash: 1886987515f3cafe38418960baa4b6fd89e3b6f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590802"
---
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="ef2f9-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ef2f9-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="ef2f9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef2f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef2f9-105">Realiza operaciones en los mensajes y subcarpetas en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ef2f9-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ef2f9-106">Header file:</span></span>  <br/> |<span data-ttu-id="ef2f9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ef2f9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ef2f9-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="ef2f9-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ef2f9-109">Objetos de carpeta</span><span class="sxs-lookup"><span data-stu-id="ef2f9-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="ef2f9-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="ef2f9-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ef2f9-111">Proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="ef2f9-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="ef2f9-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ef2f9-112">Called by:</span></span>  <br/> |<span data-ttu-id="ef2f9-113">Las aplicaciones cliente y MAPI</span><span class="sxs-lookup"><span data-stu-id="ef2f9-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="ef2f9-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="ef2f9-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ef2f9-115">IID_IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="ef2f9-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="ef2f9-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="ef2f9-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ef2f9-117">LPMAPIFOLDER</span><span class="sxs-lookup"><span data-stu-id="ef2f9-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="ef2f9-118">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="ef2f9-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="ef2f9-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="ef2f9-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ef2f9-120">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="ef2f9-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ef2f9-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="ef2f9-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="ef2f9-122">Crea un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="ef2f9-123">CopyMessages</span><span class="sxs-lookup"><span data-stu-id="ef2f9-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="ef2f9-124">Copia o mueve uno o más mensajes.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="ef2f9-125">DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="ef2f9-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="ef2f9-126">Elimina uno o más mensajes.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="ef2f9-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="ef2f9-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="ef2f9-128">Crea una nueva subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="ef2f9-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="ef2f9-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="ef2f9-130">Copia o mueve una subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="ef2f9-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="ef2f9-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="ef2f9-132">Elimina una subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="ef2f9-133">SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="ef2f9-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="ef2f9-134">Establece o borra el indicador MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uno o varios de los mensajes de la carpeta y administra el envío de informes de lectura.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="ef2f9-135">GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="ef2f9-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="ef2f9-136">Obtiene el estado asociado a un mensaje de una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="ef2f9-137">SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="ef2f9-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="ef2f9-138">Establece el estado asociado a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="ef2f9-139">SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="ef2f9-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="ef2f9-140">Establece el criterio de ordenación predeterminado para la tabla de contenido de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="ef2f9-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="ef2f9-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="ef2f9-142">Elimina todos los mensajes y subcarpetas de una carpeta sin eliminar la propia carpeta.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="ef2f9-143">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="ef2f9-143">**Required properties**</span></span>|<span data-ttu-id="ef2f9-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="ef2f9-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef2f9-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef2f9-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef2f9-146">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="ef2f9-147">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef2f9-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef2f9-148">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef2f9-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="ef2f9-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef2f9-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef2f9-150">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="ef2f9-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef2f9-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef2f9-152">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef2f9-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="ef2f9-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef2f9-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef2f9-154">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef2f9-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="ef2f9-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef2f9-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef2f9-156">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef2f9-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="ef2f9-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef2f9-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef2f9-158">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef2f9-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="ef2f9-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef2f9-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef2f9-160">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef2f9-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef2f9-161">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ef2f9-161">See also</span></span>



[<span data-ttu-id="ef2f9-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="ef2f9-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

