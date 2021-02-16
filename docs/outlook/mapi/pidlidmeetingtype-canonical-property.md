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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331580"
---
# <a name="pidlidmeetingtype-canonical-property"></a><span data-ttu-id="ae6f1-103">Propiedad canónica PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="ae6f1-103">PidLidMeetingType Canonical Property</span></span>

  
  
<span data-ttu-id="ae6f1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae6f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae6f1-105">Indica el tipo de solicitud de reunión o actualización de reunión.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-105">Indicates the type of meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ae6f1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ae6f1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ae6f1-107">dispidMeetingType</span><span class="sxs-lookup"><span data-stu-id="ae6f1-107">dispidMeetingType</span></span>  <br/> |
|<span data-ttu-id="ae6f1-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="ae6f1-108">Property set:</span></span>  <br/> |<span data-ttu-id="ae6f1-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="ae6f1-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="ae6f1-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ae6f1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ae6f1-111">0x00000026</span><span class="sxs-lookup"><span data-stu-id="ae6f1-111">0x00000026</span></span>  <br/> |
|<span data-ttu-id="ae6f1-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ae6f1-112">Data type:</span></span>  <br/> |<span data-ttu-id="ae6f1-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ae6f1-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ae6f1-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ae6f1-114">Area:</span></span>  <br/> |<span data-ttu-id="ae6f1-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="ae6f1-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae6f1-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ae6f1-116">Remarks</span></span>

<span data-ttu-id="ae6f1-117">El valor de esta propiedad debe establecerse en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="ae6f1-117">The value of this property must be set to one of the following:</span></span>
  
|<span data-ttu-id="ae6f1-118">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="ae6f1-118">**Property**</span></span>|<span data-ttu-id="ae6f1-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ae6f1-119">**Value**</span></span>|<span data-ttu-id="ae6f1-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae6f1-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ae6f1-121">mtgEmpty</span><span class="sxs-lookup"><span data-stu-id="ae6f1-121">mtgEmpty</span></span>  <br/> |<span data-ttu-id="ae6f1-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae6f1-122">0x00000000</span></span>  <br/> |<span data-ttu-id="ae6f1-123">No especificado.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-123">Unspecified.</span></span>  <br/> |
|<span data-ttu-id="ae6f1-124">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="ae6f1-124">mtgRequest</span></span>  <br/> |<span data-ttu-id="ae6f1-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ae6f1-125">0x00000001</span></span>  <br/> |<span data-ttu-id="ae6f1-126">Solicitud de reunión inicial.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-126">Initial meeting request.</span></span>  <br/> |
|<span data-ttu-id="ae6f1-127">mtgFull</span><span class="sxs-lookup"><span data-stu-id="ae6f1-127">mtgFull</span></span>  <br/> |<span data-ttu-id="ae6f1-128">0x00010000</span><span class="sxs-lookup"><span data-stu-id="ae6f1-128">0x00010000</span></span>  <br/> |<span data-ttu-id="ae6f1-129">Actualización completa.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-129">Full update.</span></span>  <br/> |
|<span data-ttu-id="ae6f1-130">mtgInfo</span><span class="sxs-lookup"><span data-stu-id="ae6f1-130">mtgInfo</span></span>  <br/> |<span data-ttu-id="ae6f1-131">0x00020000</span><span class="sxs-lookup"><span data-stu-id="ae6f1-131">0x00020000</span></span>  <br/> |<span data-ttu-id="ae6f1-132">Actualización informativo.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-132">Informational update.</span></span>  <br/> |
|<span data-ttu-id="ae6f1-133">mtgOutOfDate</span><span class="sxs-lookup"><span data-stu-id="ae6f1-133">mtgOutOfDate</span></span>  <br/> |<span data-ttu-id="ae6f1-134">0x00080000</span><span class="sxs-lookup"><span data-stu-id="ae6f1-134">0x00080000</span></span>  <br/> |<span data-ttu-id="ae6f1-135">Después de esta, se recibió una solicitud de reunión o actualización de reunión más reciente.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-135">A newer meeting request or meeting update was received after this one.</span></span>  <br/> |
|<span data-ttu-id="ae6f1-136">mtgDelegatorCopy</span><span class="sxs-lookup"><span data-stu-id="ae6f1-136">mtgDelegatorCopy</span></span>  <br/> |<span data-ttu-id="ae6f1-137">0x00100000</span><span class="sxs-lookup"><span data-stu-id="ae6f1-137">0x00100000</span></span>  <br/> |<span data-ttu-id="ae6f1-138">Esto se establece en la copia del delegador cuando un delegado controla objetos relacionados con reuniones.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-138">This is set on the delegator's copy when a delegate handles meeting-related objects.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ae6f1-139">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae6f1-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ae6f1-140">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="ae6f1-140">Protocol specifications</span></span>

<span data-ttu-id="ae6f1-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ae6f1-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ae6f1-142">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-142">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ae6f1-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ae6f1-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ae6f1-144">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ae6f1-145">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ae6f1-145">Header files</span></span>

<span data-ttu-id="ae6f1-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ae6f1-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="ae6f1-147">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-147">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ae6f1-148">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ae6f1-148">See also</span></span>



[<span data-ttu-id="ae6f1-149">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ae6f1-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ae6f1-150">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="ae6f1-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ae6f1-151">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ae6f1-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ae6f1-152">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="ae6f1-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

