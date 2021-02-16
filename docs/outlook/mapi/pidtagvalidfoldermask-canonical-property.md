---
title: Propiedad canónica PidTagValidFolderMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagValidFolderMask
api_type:
- COM
ms.assetid: 83a44aee-5269-42a8-8078-4bc063bb6e29
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 925e0eb60d55349ded114b827b6ca67e3b5ac1ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427797"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a><span data-ttu-id="5f9da-103">Propiedad canónica PidTagValidFolderMask</span><span class="sxs-lookup"><span data-stu-id="5f9da-103">PidTagValidFolderMask Canonical Property</span></span>

  
  
<span data-ttu-id="5f9da-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f9da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f9da-105">Contiene una máscara de bits de marcas que indican la validez de los identificadores de entrada de las carpetas de un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="5f9da-105">Contains a bitmask of flags that indicate the validity of the entry identifiers of the folders in a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f9da-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5f9da-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f9da-107">PR_VALID_FOLDER_MASK</span><span class="sxs-lookup"><span data-stu-id="5f9da-107">PR_VALID_FOLDER_MASK</span></span>  <br/> |
|<span data-ttu-id="5f9da-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5f9da-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5f9da-109">0x35DF</span><span class="sxs-lookup"><span data-stu-id="5f9da-109">0x35DF</span></span>  <br/> |
|<span data-ttu-id="5f9da-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5f9da-110">Data type:</span></span>  <br/> |<span data-ttu-id="5f9da-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5f9da-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5f9da-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5f9da-112">Area:</span></span>  <br/> |<span data-ttu-id="5f9da-113">Almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="5f9da-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f9da-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f9da-114">Remarks</span></span>

<span data-ttu-id="5f9da-115">El identificador de entrada de una carpeta puede volverse no válido si un usuario elimina la carpeta o si el almacén de mensajes se daña.</span><span class="sxs-lookup"><span data-stu-id="5f9da-115">A folder's entry identifier can become invalid if a user deletes the folder or if the message store becomes corrupted.</span></span>
  
<span data-ttu-id="5f9da-116">Se pueden establecer una o varias de las siguientes marcas para la máscara de bits:</span><span class="sxs-lookup"><span data-stu-id="5f9da-116">One or more of the following flags can be set for the bitmask:</span></span> 
  
<span data-ttu-id="5f9da-117">FOLDER_COMMON_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="5f9da-117">FOLDER_COMMON_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="5f9da-118">La carpeta de vistas comunes tiene un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="5f9da-118">The common views folder has a valid entry identifier.</span></span> <span data-ttu-id="5f9da-119">Vea **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5f9da-119">See **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="5f9da-120">FOLDER_FINDER_VALID</span><span class="sxs-lookup"><span data-stu-id="5f9da-120">FOLDER_FINDER_VALID</span></span> 
  
> <span data-ttu-id="5f9da-121">La carpeta finder tiene un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="5f9da-121">The finder folder has a valid entry identifier.</span></span> <span data-ttu-id="5f9da-122">Vea **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5f9da-122">See **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="5f9da-123">FOLDER_IPM_INBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="5f9da-123">FOLDER_IPM_INBOX_VALID</span></span> 
  
> <span data-ttu-id="5f9da-124">La carpeta de recepción de mensajes interpersonales (IPM) tiene un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="5f9da-124">The interpersonal message (IPM) receive folder has a valid entry identifier.</span></span> <span data-ttu-id="5f9da-125">Vea [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="5f9da-125">See [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
<span data-ttu-id="5f9da-126">FOLDER_IPM_OUTBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="5f9da-126">FOLDER_IPM_OUTBOX_VALID</span></span> 
  
> <span data-ttu-id="5f9da-127">La carpeta Bandeja de salida IPM tiene un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="5f9da-127">The IPM Outbox folder has a valid entry identifier.</span></span> <span data-ttu-id="5f9da-128">Vea **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5f9da-128">See **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="5f9da-129">FOLDER_IPM_SENTMAIL_VALID</span><span class="sxs-lookup"><span data-stu-id="5f9da-129">FOLDER_IPM_SENTMAIL_VALID</span></span> 
  
> <span data-ttu-id="5f9da-130">La carpeta Elementos enviados ipm tiene un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="5f9da-130">The IPM Sent Items folder has a valid entry identifier.</span></span> <span data-ttu-id="5f9da-131">Vea **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5f9da-131">See **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="5f9da-132">FOLDER_IPM_SUBTREE_VALID</span><span class="sxs-lookup"><span data-stu-id="5f9da-132">FOLDER_IPM_SUBTREE_VALID</span></span> 
  
> <span data-ttu-id="5f9da-133">El subárbol de carpeta IPM tiene un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="5f9da-133">The IPM folder subtree has a valid entry identifier.</span></span> <span data-ttu-id="5f9da-134">Vea **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5f9da-134">See **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="5f9da-135">FOLDER_IPM_WASTEBASKET_VALID</span><span class="sxs-lookup"><span data-stu-id="5f9da-135">FOLDER_IPM_WASTEBASKET_VALID</span></span> 
  
> <span data-ttu-id="5f9da-136">La carpeta Elementos eliminados de IPM tiene un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="5f9da-136">The IPM Deleted Items folder has a valid entry identifier.</span></span> <span data-ttu-id="5f9da-137">Vea **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5f9da-137">See **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="5f9da-138">FOLDER_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="5f9da-138">FOLDER_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="5f9da-139">La carpeta vistas tiene un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="5f9da-139">The views folder has a valid entry identifier.</span></span> <span data-ttu-id="5f9da-140">Vea **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5f9da-140">See **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="5f9da-141">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f9da-141">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5f9da-142">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5f9da-142">Header files</span></span>

<span data-ttu-id="5f9da-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f9da-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f9da-144">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5f9da-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="5f9da-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5f9da-145">Mapitags.h</span></span>
  
> <span data-ttu-id="5f9da-146">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="5f9da-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f9da-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5f9da-147">See also</span></span>



[<span data-ttu-id="5f9da-148">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5f9da-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f9da-149">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="5f9da-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f9da-150">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5f9da-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f9da-151">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="5f9da-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

