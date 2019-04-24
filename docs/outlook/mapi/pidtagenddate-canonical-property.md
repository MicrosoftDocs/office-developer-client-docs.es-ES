---
title: Propiedad canónica PidTagEndDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEndDate
api_type:
- HeaderDef
ms.assetid: d7ec5c79-1287-4364-b5e5-5d1d6f0ea0f1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2688e1764b6e4e31a47aeee306987caa66c709a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361064"
---
# <a name="pidtagenddate-canonical-property"></a><span data-ttu-id="0dff6-103">Propiedad canónica PidTagEndDate</span><span class="sxs-lookup"><span data-stu-id="0dff6-103">PidTagEndDate Canonical Property</span></span>

  
  
<span data-ttu-id="0dff6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dff6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dff6-105">Contiene la fecha y hora de finalización de una cita como administrada por una aplicación de programación.</span><span class="sxs-lookup"><span data-stu-id="0dff6-105">Contains the ending date and time of an appointment as managed by a scheduling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0dff6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0dff6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0dff6-107">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="0dff6-107">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="0dff6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0dff6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0dff6-109">0x0061</span><span class="sxs-lookup"><span data-stu-id="0dff6-109">0x0061</span></span>  <br/> |
|<span data-ttu-id="0dff6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0dff6-110">Data type:</span></span>  <br/> |<span data-ttu-id="0dff6-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="0dff6-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="0dff6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0dff6-112">Area:</span></span>  <br/> |<span data-ttu-id="0dff6-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="0dff6-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0dff6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0dff6-114">Remarks</span></span>

<span data-ttu-id="0dff6-115">La programación de aplicaciones debe establecer tanto **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) como esta propiedad al enviar las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="0dff6-115">Scheduling applications should set both the **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) and this property when sending meeting requests.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0dff6-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0dff6-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0dff6-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0dff6-117">Protocol specifications</span></span>

<span data-ttu-id="0dff6-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0dff6-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0dff6-119">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0dff6-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0dff6-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0dff6-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0dff6-121">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="0dff6-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0dff6-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0dff6-122">Header files</span></span>

<span data-ttu-id="0dff6-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0dff6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="0dff6-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0dff6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="0dff6-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0dff6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="0dff6-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0dff6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0dff6-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0dff6-127">See also</span></span>



[<span data-ttu-id="0dff6-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0dff6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0dff6-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="0dff6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0dff6-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0dff6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0dff6-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="0dff6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

