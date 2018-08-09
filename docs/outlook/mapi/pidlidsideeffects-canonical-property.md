---
title: Propiedad canónica PidLidSideEffects
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSideEffects
api_type:
- COM
ms.assetid: 90d601d9-5eeb-40b6-885d-ccd8a95ae322
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 479ba1990f7cac1768fc5e514e3fc55f017e4a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818915"
---
# <a name="pidlidsideeffects-canonical-property"></a><span data-ttu-id="ff769-103">Propiedad canónica PidLidSideEffects</span><span class="sxs-lookup"><span data-stu-id="ff769-103">PidLidSideEffects Canonical Property</span></span>

  
  
<span data-ttu-id="ff769-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ff769-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ff769-105">Controla cómo se administra un objeto de mensaje por el cliente cuando actúa en la entrada del usuario final.</span><span class="sxs-lookup"><span data-stu-id="ff769-105">Controls how a message object is handled by the client when acting on end-user input.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ff769-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ff769-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ff769-107">dispidSideEffects</span><span class="sxs-lookup"><span data-stu-id="ff769-107">dispidSideEffects</span></span>  <br/> |
|<span data-ttu-id="ff769-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="ff769-108">Property set:</span></span>  <br/> |<span data-ttu-id="ff769-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ff769-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ff769-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="ff769-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ff769-111">0x00008510</span><span class="sxs-lookup"><span data-stu-id="ff769-111">0x00008510</span></span>  <br/> |
|<span data-ttu-id="ff769-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ff769-112">Data type:</span></span>  <br/> |<span data-ttu-id="ff769-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ff769-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ff769-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ff769-114">Area:</span></span>  <br/> |<span data-ttu-id="ff769-115">Configuración de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="ff769-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff769-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ff769-116">Remarks</span></span>

<span data-ttu-id="ff769-117">Se debe establecer en un bit a bit o cero o más de las siguientes marcas.</span><span class="sxs-lookup"><span data-stu-id="ff769-117">Must be set to a bitwise or zero or more of the following flags.</span></span>
  
|<span data-ttu-id="ff769-118">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="ff769-118">**Name**</span></span>|<span data-ttu-id="ff769-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ff769-119">**Value**</span></span>|<span data-ttu-id="ff769-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ff769-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ff769-121">seOpenToDelete</span><span class="sxs-lookup"><span data-stu-id="ff769-121">seOpenToDelete</span></span>  <br/> |<span data-ttu-id="ff769-122">0 x 0001</span><span class="sxs-lookup"><span data-stu-id="ff769-122">0x0001</span></span>  <br/> |<span data-ttu-id="ff769-123">Al eliminar, se requiere procesamiento adicional en el objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ff769-123">Additional processing is required on the message object when deleting.</span></span>  <br/> |
|<span data-ttu-id="ff769-124">seNoFrame</span><span class="sxs-lookup"><span data-stu-id="ff769-124">seNoFrame</span></span>  <br/> |<span data-ttu-id="ff769-125">0x0008</span><span class="sxs-lookup"><span data-stu-id="ff769-125">0x0008</span></span>  <br/> |<span data-ttu-id="ff769-126">Interfaz de usuario no está asociado con el objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ff769-126">No UI is associated with the message object.</span></span>  <br/> |
|<span data-ttu-id="ff769-127">seCoerceToInbox</span><span class="sxs-lookup"><span data-stu-id="ff769-127">seCoerceToInbox</span></span>  <br/> |<span data-ttu-id="ff769-128">0x0010</span><span class="sxs-lookup"><span data-stu-id="ff769-128">0x0010</span></span>  <br/> |<span data-ttu-id="ff769-129">Se requiere procesamiento adicional en el objeto de mensaje al mover o copiar a un objeto de carpeta con una propiedad de **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) de "IPF. Tenga en cuenta".</span><span class="sxs-lookup"><span data-stu-id="ff769-129">Additional processing is required on the message object when moving or copying to a folder object with a **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) property of "IPF.Note".</span></span>  <br/> |
|<span data-ttu-id="ff769-130">seOpenTocopy</span><span class="sxs-lookup"><span data-stu-id="ff769-130">seOpenTocopy</span></span>  <br/> |<span data-ttu-id="ff769-131">0 x 0020</span><span class="sxs-lookup"><span data-stu-id="ff769-131">0x0020</span></span>  <br/> |<span data-ttu-id="ff769-132">Se requiere procesamiento adicional en el objeto de mensaje cuando se copian a otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="ff769-132">Additional processing is required on the message object when copying to another folder.</span></span>  <br/> |
|<span data-ttu-id="ff769-133">seOpenToMove</span><span class="sxs-lookup"><span data-stu-id="ff769-133">seOpenToMove</span></span>  <br/> |<span data-ttu-id="ff769-134">0x0040</span><span class="sxs-lookup"><span data-stu-id="ff769-134">0x0040</span></span>  <br/> |<span data-ttu-id="ff769-135">Se requiere procesamiento adicional en el objeto de mensaje cuando se mueve a otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="ff769-135">Additional processing is required on the message object when moving to another folder.</span></span>  <br/> |
|<span data-ttu-id="ff769-136">seOpenForCtxMenu</span><span class="sxs-lookup"><span data-stu-id="ff769-136">seOpenForCtxMenu</span></span>  <br/> |<span data-ttu-id="ff769-137">0 x 0100</span><span class="sxs-lookup"><span data-stu-id="ff769-137">0x0100</span></span>  <br/> |<span data-ttu-id="ff769-138">Se requiere procesamiento adicional en el objeto de mensaje al mostrar los verbos para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="ff769-138">Additional processing is required on the message object when displaying verbs to the end-user.</span></span>  <br/> |
|<span data-ttu-id="ff769-139">seCannotUndoDelete</span><span class="sxs-lookup"><span data-stu-id="ff769-139">seCannotUndoDelete</span></span>  <br/> |<span data-ttu-id="ff769-140">0 x 0400</span><span class="sxs-lookup"><span data-stu-id="ff769-140">0x0400</span></span>  <br/> |<span data-ttu-id="ff769-141">No se puede deshacer la operación de eliminación, no debe estar establecida a menos que se establezca "seOpenToDelete".</span><span class="sxs-lookup"><span data-stu-id="ff769-141">Cannot undo delete operation, must not be set unless "seOpenToDelete" is set.</span></span>  <br/> |
|<span data-ttu-id="ff769-142">seCannotUndoCopy</span><span class="sxs-lookup"><span data-stu-id="ff769-142">seCannotUndoCopy</span></span>  <br/> |<span data-ttu-id="ff769-143">0 x 0800</span><span class="sxs-lookup"><span data-stu-id="ff769-143">0x0800</span></span>  <br/> |<span data-ttu-id="ff769-144">No se puede deshacer la operación de copia, no debe estar establecida a menos que se establezca "seOpenTocopy".</span><span class="sxs-lookup"><span data-stu-id="ff769-144">Cannot undo copy operation, must not be set unless "seOpenTocopy" is set.</span></span>  <br/> |
|<span data-ttu-id="ff769-145">seCannotUndoMove</span><span class="sxs-lookup"><span data-stu-id="ff769-145">seCannotUndoMove</span></span>  <br/> |<span data-ttu-id="ff769-146">0 x 1000</span><span class="sxs-lookup"><span data-stu-id="ff769-146">0x1000</span></span>  <br/> |<span data-ttu-id="ff769-147">No se puede deshacer la operación de movimiento, no debe estar establecida a menos que se establezca "seOpenToMove".</span><span class="sxs-lookup"><span data-stu-id="ff769-147">Cannot undo move operation, must not be set unless "seOpenToMove" is set.</span></span>  <br/> |
|<span data-ttu-id="ff769-148">seHasScript</span><span class="sxs-lookup"><span data-stu-id="ff769-148">seHasScript</span></span>  <br/> |<span data-ttu-id="ff769-149">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="ff769-149">0x2000</span></span>  <br/> |<span data-ttu-id="ff769-150">El objeto de mensaje contiene secuencias de comandos de usuario final.</span><span class="sxs-lookup"><span data-stu-id="ff769-150">The message object contains end-user script.</span></span>  <br/> |
|<span data-ttu-id="ff769-151">seOpenToPermDelete</span><span class="sxs-lookup"><span data-stu-id="ff769-151">seOpenToPermDelete</span></span>  <br/> |<span data-ttu-id="ff769-152">0 x 4000</span><span class="sxs-lookup"><span data-stu-id="ff769-152">0x4000</span></span>  <br/> |<span data-ttu-id="ff769-153">Se requiere procesamiento adicional para eliminar permanentemente el objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ff769-153">Additional processing is required to permanently delete the message object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ff769-154">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff769-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ff769-155">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="ff769-155">Protocol specifications</span></span>

<span data-ttu-id="ff769-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff769-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff769-157">Proporciona la definición del conjunto de propiedad y referencias a las especificaciones de protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ff769-157">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ff769-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff769-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff769-159">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ff769-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="ff769-160">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff769-160">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff769-161">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="ff769-161">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ff769-162">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ff769-162">Header files</span></span>

<span data-ttu-id="ff769-163">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ff769-163">Mapidefs.h</span></span>
  
> <span data-ttu-id="ff769-164">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ff769-164">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff769-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff769-165">See also</span></span>



[<span data-ttu-id="ff769-166">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ff769-166">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ff769-167">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="ff769-167">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ff769-168">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ff769-168">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ff769-169">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="ff769-169">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

