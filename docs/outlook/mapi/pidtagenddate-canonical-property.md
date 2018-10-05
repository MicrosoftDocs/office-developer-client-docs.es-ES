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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382718"
---
# <a name="pidtagenddate-canonical-property"></a><span data-ttu-id="74262-103">Propiedad canónica PidTagEndDate</span><span class="sxs-lookup"><span data-stu-id="74262-103">PidTagEndDate Canonical Property</span></span>

  
  
<span data-ttu-id="74262-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74262-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74262-105">Contiene la fecha final y la hora de una cita como administrado por una aplicación de programación.</span><span class="sxs-lookup"><span data-stu-id="74262-105">Contains the ending date and time of an appointment as managed by a scheduling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="74262-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="74262-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74262-107">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="74262-107">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="74262-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="74262-108">Identifier:</span></span>  <br/> |<span data-ttu-id="74262-109">0x0061</span><span class="sxs-lookup"><span data-stu-id="74262-109">0x0061</span></span>  <br/> |
|<span data-ttu-id="74262-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="74262-110">Data type:</span></span>  <br/> |<span data-ttu-id="74262-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="74262-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="74262-112">Área:</span><span class="sxs-lookup"><span data-stu-id="74262-112">Area:</span></span>  <br/> |<span data-ttu-id="74262-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="74262-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74262-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74262-114">Remarks</span></span>

<span data-ttu-id="74262-115">Programación de aplicaciones debe establecer **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) y esta propiedad al enviar convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="74262-115">Scheduling applications should set both the **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) and this property when sending meeting requests.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="74262-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="74262-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="74262-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="74262-117">Protocol specifications</span></span>

<span data-ttu-id="74262-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74262-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74262-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="74262-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="74262-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74262-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74262-121">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="74262-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="74262-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="74262-122">Header files</span></span>

<span data-ttu-id="74262-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74262-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="74262-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="74262-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="74262-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="74262-125">Mapitags.h</span></span>
  
> <span data-ttu-id="74262-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="74262-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74262-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="74262-127">See also</span></span>



[<span data-ttu-id="74262-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="74262-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74262-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="74262-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74262-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="74262-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74262-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="74262-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

