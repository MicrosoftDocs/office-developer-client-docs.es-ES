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
ms.openlocfilehash: 2d57e6a195036ead9eb42666876e91a72f65eb8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331300"
---
# <a name="pidlidsideeffects-canonical-property"></a><span data-ttu-id="e158d-103">Propiedad canónica PidLidSideEffects</span><span class="sxs-lookup"><span data-stu-id="e158d-103">PidLidSideEffects Canonical Property</span></span>

  
  
<span data-ttu-id="e158d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e158d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e158d-105">Controla el modo en que el cliente controla un objeto de mensaje al actuar en la entrada del usuario final.</span><span class="sxs-lookup"><span data-stu-id="e158d-105">Controls how a message object is handled by the client when acting on end-user input.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e158d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e158d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e158d-107">dispidSideEffects</span><span class="sxs-lookup"><span data-stu-id="e158d-107">dispidSideEffects</span></span>  <br/> |
|<span data-ttu-id="e158d-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e158d-108">Property set:</span></span>  <br/> |<span data-ttu-id="e158d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e158d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e158d-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e158d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e158d-111">0x00008510</span><span class="sxs-lookup"><span data-stu-id="e158d-111">0x00008510</span></span>  <br/> |
|<span data-ttu-id="e158d-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e158d-112">Data type:</span></span>  <br/> |<span data-ttu-id="e158d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e158d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e158d-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e158d-114">Area:</span></span>  <br/> |<span data-ttu-id="e158d-115">Configuración en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="e158d-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e158d-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e158d-116">Remarks</span></span>

<span data-ttu-id="e158d-117">Debe establecerse en un bit a bit o en cero o más de las siguientes marcas.</span><span class="sxs-lookup"><span data-stu-id="e158d-117">Must be set to a bitwise or zero or more of the following flags.</span></span>
  
|<span data-ttu-id="e158d-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="e158d-118">**Name**</span></span>|<span data-ttu-id="e158d-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e158d-119">**Value**</span></span>|<span data-ttu-id="e158d-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e158d-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e158d-121">seOpenToDelete</span><span class="sxs-lookup"><span data-stu-id="e158d-121">seOpenToDelete</span></span>  <br/> |<span data-ttu-id="e158d-122">0x0001</span><span class="sxs-lookup"><span data-stu-id="e158d-122">0x0001</span></span>  <br/> |<span data-ttu-id="e158d-123">Se requiere procesamiento adicional en el objeto de mensaje al eliminar.</span><span class="sxs-lookup"><span data-stu-id="e158d-123">Additional processing is required on the message object when deleting.</span></span>  <br/> |
|<span data-ttu-id="e158d-124">seNoFrame</span><span class="sxs-lookup"><span data-stu-id="e158d-124">seNoFrame</span></span>  <br/> |<span data-ttu-id="e158d-125">0x0008</span><span class="sxs-lookup"><span data-stu-id="e158d-125">0x0008</span></span>  <br/> |<span data-ttu-id="e158d-126">No hay ninguna interfaz de usuario asociada con el objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e158d-126">No UI is associated with the message object.</span></span>  <br/> |
|<span data-ttu-id="e158d-127">seCoerceToInbox</span><span class="sxs-lookup"><span data-stu-id="e158d-127">seCoerceToInbox</span></span>  <br/> |<span data-ttu-id="e158d-128">0x0010</span><span class="sxs-lookup"><span data-stu-id="e158d-128">0x0010</span></span>  <br/> |<span data-ttu-id="e158d-129">Se requiere procesamiento adicional en el objeto de mensaje al mover o copiar a un objeto de carpeta con una propiedad **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) de "IPF. Nota".</span><span class="sxs-lookup"><span data-stu-id="e158d-129">Additional processing is required on the message object when moving or copying to a folder object with a **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) property of "IPF.Note".</span></span>  <br/> |
|<span data-ttu-id="e158d-130">seOpenTocopy</span><span class="sxs-lookup"><span data-stu-id="e158d-130">seOpenTocopy</span></span>  <br/> |<span data-ttu-id="e158d-131">0x0020</span><span class="sxs-lookup"><span data-stu-id="e158d-131">0x0020</span></span>  <br/> |<span data-ttu-id="e158d-132">Se requiere procesamiento adicional en el objeto de mensaje al copiar en otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="e158d-132">Additional processing is required on the message object when copying to another folder.</span></span>  <br/> |
|<span data-ttu-id="e158d-133">seOpenToMove</span><span class="sxs-lookup"><span data-stu-id="e158d-133">seOpenToMove</span></span>  <br/> |<span data-ttu-id="e158d-134">0x0040</span><span class="sxs-lookup"><span data-stu-id="e158d-134">0x0040</span></span>  <br/> |<span data-ttu-id="e158d-135">Se requiere procesamiento adicional en el objeto de mensaje cuando se mueve a otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="e158d-135">Additional processing is required on the message object when moving to another folder.</span></span>  <br/> |
|<span data-ttu-id="e158d-136">seOpenForCtxMenu</span><span class="sxs-lookup"><span data-stu-id="e158d-136">seOpenForCtxMenu</span></span>  <br/> |<span data-ttu-id="e158d-137">0x0100</span><span class="sxs-lookup"><span data-stu-id="e158d-137">0x0100</span></span>  <br/> |<span data-ttu-id="e158d-138">Se requiere procesamiento adicional en el objeto de mensaje al mostrar verbos al usuario final.</span><span class="sxs-lookup"><span data-stu-id="e158d-138">Additional processing is required on the message object when displaying verbs to the end-user.</span></span>  <br/> |
|<span data-ttu-id="e158d-139">seCannotUndoDelete</span><span class="sxs-lookup"><span data-stu-id="e158d-139">seCannotUndoDelete</span></span>  <br/> |<span data-ttu-id="e158d-140">0x0400</span><span class="sxs-lookup"><span data-stu-id="e158d-140">0x0400</span></span>  <br/> |<span data-ttu-id="e158d-141">No se puede deshacer la operación de eliminación, no se debe establecer a menos que se establezca "seOpenToDelete".</span><span class="sxs-lookup"><span data-stu-id="e158d-141">Cannot undo delete operation, must not be set unless "seOpenToDelete" is set.</span></span>  <br/> |
|<span data-ttu-id="e158d-142">seCannotUndoCopy</span><span class="sxs-lookup"><span data-stu-id="e158d-142">seCannotUndoCopy</span></span>  <br/> |<span data-ttu-id="e158d-143">0x0800</span><span class="sxs-lookup"><span data-stu-id="e158d-143">0x0800</span></span>  <br/> |<span data-ttu-id="e158d-144">No se puede deshacer la operación de copia, no se debe establecer a menos que se establezca "seOpenTocopy".</span><span class="sxs-lookup"><span data-stu-id="e158d-144">Cannot undo copy operation, must not be set unless "seOpenTocopy" is set.</span></span>  <br/> |
|<span data-ttu-id="e158d-145">seCannotUndoMove</span><span class="sxs-lookup"><span data-stu-id="e158d-145">seCannotUndoMove</span></span>  <br/> |<span data-ttu-id="e158d-146">0x1000</span><span class="sxs-lookup"><span data-stu-id="e158d-146">0x1000</span></span>  <br/> |<span data-ttu-id="e158d-147">No se puede deshacer la operación de movimiento, no se debe establecer a menos que se establezca "seOpenToMove".</span><span class="sxs-lookup"><span data-stu-id="e158d-147">Cannot undo move operation, must not be set unless "seOpenToMove" is set.</span></span>  <br/> |
|<span data-ttu-id="e158d-148">seHasScript</span><span class="sxs-lookup"><span data-stu-id="e158d-148">seHasScript</span></span>  <br/> |<span data-ttu-id="e158d-149">0x2000</span><span class="sxs-lookup"><span data-stu-id="e158d-149">0x2000</span></span>  <br/> |<span data-ttu-id="e158d-150">El objeto de mensaje contiene un script de usuario final.</span><span class="sxs-lookup"><span data-stu-id="e158d-150">The message object contains end-user script.</span></span>  <br/> |
|<span data-ttu-id="e158d-151">seOpenToPermDelete</span><span class="sxs-lookup"><span data-stu-id="e158d-151">seOpenToPermDelete</span></span>  <br/> |<span data-ttu-id="e158d-152">0x4000</span><span class="sxs-lookup"><span data-stu-id="e158d-152">0x4000</span></span>  <br/> |<span data-ttu-id="e158d-153">Se requiere un procesamiento adicional para eliminar permanentemente el objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e158d-153">Additional processing is required to permanently delete the message object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e158d-154">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e158d-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e158d-155">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="e158d-155">Protocol specifications</span></span>

<span data-ttu-id="e158d-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e158d-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e158d-157">Proporciona la definición del conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="e158d-157">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e158d-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e158d-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e158d-159">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e158d-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e158d-160">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e158d-160">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e158d-161">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="e158d-161">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e158d-162">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e158d-162">Header files</span></span>

<span data-ttu-id="e158d-163">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e158d-163">Mapidefs.h</span></span>
  
> <span data-ttu-id="e158d-164">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e158d-164">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e158d-165">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e158d-165">See also</span></span>



[<span data-ttu-id="e158d-166">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e158d-166">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e158d-167">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="e158d-167">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e158d-168">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e158d-168">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e158d-169">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="e158d-169">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

