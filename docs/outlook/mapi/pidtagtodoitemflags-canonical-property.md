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
ms.openlocfilehash: 6ddc7231afef0a224b92be7fe86216e56200ab70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284486"
---
# <a name="pidtagtodoitemflags-canonical-property"></a><span data-ttu-id="54dc1-103">Propiedad canónica PidTagToDoItemFlags</span><span class="sxs-lookup"><span data-stu-id="54dc1-103">PidTagToDoItemFlags Canonical Property</span></span>

  
  
<span data-ttu-id="54dc1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54dc1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54dc1-105">Representa la To-Do marcada de un elemento.</span><span class="sxs-lookup"><span data-stu-id="54dc1-105">Represents a To-Do item's flagged condition.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="54dc1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="54dc1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="54dc1-107">PR_TODO_ITEM_FLAGS</span><span class="sxs-lookup"><span data-stu-id="54dc1-107">PR_TODO_ITEM_FLAGS</span></span>  <br/> |
|<span data-ttu-id="54dc1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="54dc1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="54dc1-109">0x0E2B</span><span class="sxs-lookup"><span data-stu-id="54dc1-109">0x0E2B</span></span>  <br/> |
|<span data-ttu-id="54dc1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="54dc1-110">Data type:</span></span>  <br/> |<span data-ttu-id="54dc1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="54dc1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="54dc1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="54dc1-112">Area:</span></span>  <br/> |<span data-ttu-id="54dc1-113">MAPI no transmitible</span><span class="sxs-lookup"><span data-stu-id="54dc1-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54dc1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54dc1-114">Remarks</span></span>

<span data-ttu-id="54dc1-115">Esta propiedad es un campo de bits en el que cada bit debe establecerse en 1 si se aplica la condición asociada en la tabla siguiente, de lo contrario 0.</span><span class="sxs-lookup"><span data-stu-id="54dc1-115">This property is a bit field in which each bit should be set to 1 if the associated condition in the following table applies, otherwise 0.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="54dc1-116">Valor numérico</span><span class="sxs-lookup"><span data-stu-id="54dc1-116">Numeric value</span></span>  <br/> |<span data-ttu-id="54dc1-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="54dc1-117">Name</span></span>  <br/> |<span data-ttu-id="54dc1-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="54dc1-118">Description</span></span>  <br/> |
|<span data-ttu-id="54dc1-119">No presente</span><span class="sxs-lookup"><span data-stu-id="54dc1-119">Not present</span></span>  <br/> |<span data-ttu-id="54dc1-120">N/D</span><span class="sxs-lookup"><span data-stu-id="54dc1-120">N/A</span></span>  <br/> |<span data-ttu-id="54dc1-121">Sinflagged</span><span class="sxs-lookup"><span data-stu-id="54dc1-121">Unflagged</span></span>  <br/> |
|<span data-ttu-id="54dc1-122">1</span><span class="sxs-lookup"><span data-stu-id="54dc1-122">1</span></span>  <br/> |<span data-ttu-id="54dc1-123">todoTimeFlagged</span><span class="sxs-lookup"><span data-stu-id="54dc1-123">todoTimeFlagged</span></span>  <br/> |<span data-ttu-id="54dc1-124">El objeto está marcado por tiempo</span><span class="sxs-lookup"><span data-stu-id="54dc1-124">Object is time flagged</span></span>  <br/> |
|<span data-ttu-id="54dc1-125">8 </span><span class="sxs-lookup"><span data-stu-id="54dc1-125">8</span></span>  <br/> |<span data-ttu-id="54dc1-126">todoRecipientFlagged</span><span class="sxs-lookup"><span data-stu-id="54dc1-126">todoRecipientFlagged</span></span>  <br/> |<span data-ttu-id="54dc1-127">Solo se debe establecer en un objeto de borrador de mensaje y significa que el objeto está marcado para los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="54dc1-127">Should only be set on a draft message object, and it means that the object is flagged for recipients.</span></span>  <br/> |
   
<span data-ttu-id="54dc1-128">Todos los bits que no se especifican en la tabla están reservados.</span><span class="sxs-lookup"><span data-stu-id="54dc1-128">All bits that are not specified in the table are reserved.</span></span> <span data-ttu-id="54dc1-129">Deben omitirse, pero deben conservarse si se establecen.</span><span class="sxs-lookup"><span data-stu-id="54dc1-129">They must be ignored, but should be preserved if they are set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="54dc1-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="54dc1-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="54dc1-131">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="54dc1-131">Protocol specifications</span></span>

<span data-ttu-id="54dc1-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54dc1-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54dc1-133">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="54dc1-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="54dc1-134">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54dc1-134">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54dc1-135">Especifica las propiedades y las operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="54dc1-135">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="54dc1-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="54dc1-136">Header files</span></span>

<span data-ttu-id="54dc1-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54dc1-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="54dc1-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="54dc1-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="54dc1-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="54dc1-139">Mapitags.h</span></span>
  
> <span data-ttu-id="54dc1-140">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="54dc1-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54dc1-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="54dc1-141">See also</span></span>



[<span data-ttu-id="54dc1-142">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="54dc1-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="54dc1-143">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="54dc1-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="54dc1-144">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="54dc1-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="54dc1-145">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="54dc1-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

