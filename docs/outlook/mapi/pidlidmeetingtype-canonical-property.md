---
title: Propiedad canónica PidLidMeetingType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidMeetingType
api_type:
- COM
ms.assetid: 290b290c-7836-4a7e-bf1a-8d0225a07e56
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d2b00c67984d090274a17028ee74e46bee482e2b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399637"
---
# <a name="pidlidmeetingtype-canonical-property"></a><span data-ttu-id="21884-103">Propiedad canónica PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="21884-103">PidLidMeetingType Canonical Property</span></span>

  
  
<span data-ttu-id="21884-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21884-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21884-105">Indica el tipo de convocatoria de reunión o una actualización de reunión.</span><span class="sxs-lookup"><span data-stu-id="21884-105">Indicates the type of meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="21884-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="21884-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="21884-107">dispidMeetingType</span><span class="sxs-lookup"><span data-stu-id="21884-107">dispidMeetingType</span></span>  <br/> |
|<span data-ttu-id="21884-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="21884-108">Property set:</span></span>  <br/> |<span data-ttu-id="21884-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="21884-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="21884-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="21884-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="21884-111">0x00000026</span><span class="sxs-lookup"><span data-stu-id="21884-111">0x00000026</span></span>  <br/> |
|<span data-ttu-id="21884-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="21884-112">Data type:</span></span>  <br/> |<span data-ttu-id="21884-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="21884-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="21884-114">Área:</span><span class="sxs-lookup"><span data-stu-id="21884-114">Area:</span></span>  <br/> |<span data-ttu-id="21884-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="21884-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21884-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="21884-116">Remarks</span></span>

<span data-ttu-id="21884-117">El valor de esta propiedad debe establecerse en uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="21884-117">The value of this property must be set to one of the following:</span></span>
  
|<span data-ttu-id="21884-118">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="21884-118">**Property**</span></span>|<span data-ttu-id="21884-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="21884-119">**Value**</span></span>|<span data-ttu-id="21884-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="21884-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="21884-121">mtgEmpty</span><span class="sxs-lookup"><span data-stu-id="21884-121">mtgEmpty</span></span>  <br/> |<span data-ttu-id="21884-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21884-122">0x00000000</span></span>  <br/> |<span data-ttu-id="21884-123">No se especifica.</span><span class="sxs-lookup"><span data-stu-id="21884-123">Unspecified.</span></span>  <br/> |
|<span data-ttu-id="21884-124">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="21884-124">mtgRequest</span></span>  <br/> |<span data-ttu-id="21884-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="21884-125">0x00000001</span></span>  <br/> |<span data-ttu-id="21884-126">Convocatoria de reunión inicial.</span><span class="sxs-lookup"><span data-stu-id="21884-126">Initial meeting request.</span></span>  <br/> |
|<span data-ttu-id="21884-127">mtgFull</span><span class="sxs-lookup"><span data-stu-id="21884-127">mtgFull</span></span>  <br/> |<span data-ttu-id="21884-128">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="21884-128">0x00010000</span></span>  <br/> |<span data-ttu-id="21884-129">Actualización completa.</span><span class="sxs-lookup"><span data-stu-id="21884-129">Full update.</span></span>  <br/> |
|<span data-ttu-id="21884-130">mtgInfo</span><span class="sxs-lookup"><span data-stu-id="21884-130">mtgInfo</span></span>  <br/> |<span data-ttu-id="21884-131">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="21884-131">0x00020000</span></span>  <br/> |<span data-ttu-id="21884-132">Información de la actualización.</span><span class="sxs-lookup"><span data-stu-id="21884-132">Informational update.</span></span>  <br/> |
|<span data-ttu-id="21884-133">mtgOutOfDate</span><span class="sxs-lookup"><span data-stu-id="21884-133">mtgOutOfDate</span></span>  <br/> |<span data-ttu-id="21884-134">0 x 00080000</span><span class="sxs-lookup"><span data-stu-id="21884-134">0x00080000</span></span>  <br/> |<span data-ttu-id="21884-135">Una convocatoria de reunión más reciente o la actualización de la reunión se recibió después de éste.</span><span class="sxs-lookup"><span data-stu-id="21884-135">A newer meeting request or meeting update was received after this one.</span></span>  <br/> |
|<span data-ttu-id="21884-136">mtgDelegatorCopy</span><span class="sxs-lookup"><span data-stu-id="21884-136">mtgDelegatorCopy</span></span>  <br/> |<span data-ttu-id="21884-137">0 x 00100000</span><span class="sxs-lookup"><span data-stu-id="21884-137">0x00100000</span></span>  <br/> |<span data-ttu-id="21884-138">Esto se establece en la copia de la persona que delega cuando un objetos relacionados con la reunión de identificadores de delegado.</span><span class="sxs-lookup"><span data-stu-id="21884-138">This is set on the delegator's copy when a delegate handles meeting-related objects.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="21884-139">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="21884-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="21884-140">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="21884-140">Protocol specifications</span></span>

<span data-ttu-id="21884-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21884-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21884-142">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="21884-142">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="21884-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21884-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21884-144">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="21884-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="21884-145">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="21884-145">Header files</span></span>

<span data-ttu-id="21884-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="21884-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="21884-147">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="21884-147">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="21884-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="21884-148">See also</span></span>



[<span data-ttu-id="21884-149">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="21884-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="21884-150">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="21884-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="21884-151">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="21884-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="21884-152">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="21884-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

