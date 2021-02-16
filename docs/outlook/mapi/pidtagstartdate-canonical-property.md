---
title: Propiedad canónica PidTagStartDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStartDate
api_type:
- COM
ms.assetid: 908c2d9f-53f4-4aa8-b309-2f3ac2dca5b5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fd799a3dc5ba91d388285f649cccfeec188b6143
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278823"
---
# <a name="pidtagstartdate-canonical-property"></a><span data-ttu-id="01e6f-103">Propiedad canónica PidTagStartDate</span><span class="sxs-lookup"><span data-stu-id="01e6f-103">PidTagStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="01e6f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01e6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01e6f-105">Contiene la fecha y hora de inicio de una cita administrada por una aplicación de programación.</span><span class="sxs-lookup"><span data-stu-id="01e6f-105">Contains the starting date and time of an appointment as managed by a scheduling application.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="01e6f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="01e6f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="01e6f-107">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="01e6f-107">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="01e6f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="01e6f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="01e6f-109">0x0060</span><span class="sxs-lookup"><span data-stu-id="01e6f-109">0x0060</span></span>  <br/> |
|<span data-ttu-id="01e6f-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="01e6f-110">Data type:</span></span>  <br/> |<span data-ttu-id="01e6f-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="01e6f-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="01e6f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="01e6f-112">Area:</span></span>  <br/> |<span data-ttu-id="01e6f-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="01e6f-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01e6f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="01e6f-114">Remarks</span></span>

<span data-ttu-id="01e6f-115">Las aplicaciones de programación deben establecer esta propiedad **y PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) al enviar solicitudes de reunión.</span><span class="sxs-lookup"><span data-stu-id="01e6f-115">Scheduling applications should set both this property and **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) properties when sending meeting requests.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="01e6f-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="01e6f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="01e6f-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="01e6f-117">Protocol specifications</span></span>

<span data-ttu-id="01e6f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01e6f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01e6f-119">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="01e6f-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="01e6f-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01e6f-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01e6f-121">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="01e6f-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="01e6f-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="01e6f-122">Header files</span></span>

<span data-ttu-id="01e6f-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="01e6f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="01e6f-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="01e6f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="01e6f-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="01e6f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="01e6f-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="01e6f-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="01e6f-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="01e6f-127">See also</span></span>



[<span data-ttu-id="01e6f-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="01e6f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="01e6f-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="01e6f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="01e6f-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="01e6f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="01e6f-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="01e6f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

