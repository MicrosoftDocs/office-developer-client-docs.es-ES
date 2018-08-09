---
title: Propiedad canónica PidTagToDoItemFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagToDoItemFlags
api_type:
- COM
ms.assetid: bb7ccb45-ce08-4d22-9259-db15cd267e34
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cae4ef6e4d7634ca2b429eb946aa948f5d90cd92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820426"
---
# <a name="pidtagtodoitemflags-canonical-property"></a><span data-ttu-id="e1358-103">Propiedad canónica PidTagToDoItemFlags</span><span class="sxs-lookup"><span data-stu-id="e1358-103">PidTagToDoItemFlags Canonical Property</span></span>

  
  
<span data-ttu-id="e1358-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e1358-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e1358-105">Representa la condición marcado del elemento de tareas pendientes.</span><span class="sxs-lookup"><span data-stu-id="e1358-105">Represents a To-Do item's flagged condition.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1358-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e1358-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1358-107">PR_TODO_ITEM_FLAGS</span><span class="sxs-lookup"><span data-stu-id="e1358-107">PR_TODO_ITEM_FLAGS</span></span>  <br/> |
|<span data-ttu-id="e1358-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e1358-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e1358-109">0x0E2B</span><span class="sxs-lookup"><span data-stu-id="e1358-109">0x0E2B</span></span>  <br/> |
|<span data-ttu-id="e1358-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e1358-110">Data type:</span></span>  <br/> |<span data-ttu-id="e1358-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e1358-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e1358-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e1358-112">Area:</span></span>  <br/> |<span data-ttu-id="e1358-113">MAPI no transmisible</span><span class="sxs-lookup"><span data-stu-id="e1358-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1358-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e1358-114">Remarks</span></span>

<span data-ttu-id="e1358-115">Esta propiedad es un campo de bits en el que cada bit debe establecerse en 1 si se aplica la condición asociada en la tabla siguiente, en caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="e1358-115">This property is a bit field in which each bit should be set to 1 if the associated condition in the following table applies, otherwise 0.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="e1358-116">Valor numérico</span><span class="sxs-lookup"><span data-stu-id="e1358-116">Numeric value</span></span>  <br/> |<span data-ttu-id="e1358-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="e1358-117">Name</span></span>  <br/> |<span data-ttu-id="e1358-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1358-118">Description</span></span>  <br/> |
|<span data-ttu-id="e1358-119">No está presente</span><span class="sxs-lookup"><span data-stu-id="e1358-119">Not present</span></span>  <br/> |<span data-ttu-id="e1358-120">N/D</span><span class="sxs-lookup"><span data-stu-id="e1358-120">N/A</span></span>  <br/> |<span data-ttu-id="e1358-121">Sin marca</span><span class="sxs-lookup"><span data-stu-id="e1358-121">Unflagged</span></span>  <br/> |
|<span data-ttu-id="e1358-122">1</span><span class="sxs-lookup"><span data-stu-id="e1358-122">1</span></span>  <br/> |<span data-ttu-id="e1358-123">todoTimeFlagged</span><span class="sxs-lookup"><span data-stu-id="e1358-123">todoTimeFlagged</span></span>  <br/> |<span data-ttu-id="e1358-124">Objeto es marcada de hora</span><span class="sxs-lookup"><span data-stu-id="e1358-124">Object is time flagged</span></span>  <br/> |
|<span data-ttu-id="e1358-125">8</span><span class="sxs-lookup"><span data-stu-id="e1358-125">8</span></span>  <br/> |<span data-ttu-id="e1358-126">todoRecipientFlagged</span><span class="sxs-lookup"><span data-stu-id="e1358-126">todoRecipientFlagged</span></span>  <br/> |<span data-ttu-id="e1358-127">Sólo se debe establecer en un objeto de mensaje de borrador y significa que el objeto se marca para los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="e1358-127">Should only be set on a draft message object, and it means that the object is flagged for recipients.</span></span>  <br/> |
   
<span data-ttu-id="e1358-128">Se reservan todos los bits que no se especifican en la tabla.</span><span class="sxs-lookup"><span data-stu-id="e1358-128">All bits that are not specified in the table are reserved.</span></span> <span data-ttu-id="e1358-129">Debe omitirse, pero deben conservarse si se han establecido.</span><span class="sxs-lookup"><span data-stu-id="e1358-129">They must be ignored, but should be preserved if they are set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e1358-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1358-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1358-131">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e1358-131">Protocol specifications</span></span>

<span data-ttu-id="e1358-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1358-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1358-133">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e1358-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e1358-134">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1358-134">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1358-135">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="e1358-135">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1358-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e1358-136">Header files</span></span>

<span data-ttu-id="e1358-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1358-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1358-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e1358-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="e1358-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e1358-139">Mapitags.h</span></span>
  
> <span data-ttu-id="e1358-140">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="e1358-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1358-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1358-141">See also</span></span>



[<span data-ttu-id="e1358-142">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e1358-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1358-143">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e1358-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1358-144">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e1358-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1358-145">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e1358-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

