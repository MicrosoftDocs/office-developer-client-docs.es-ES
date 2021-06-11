---
title: Propiedad canónica PidTagScheduleInfoDisallowRecurringAppts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowRecurringAppts
api_type:
- COM
ms.assetid: 61e082dd-f5bc-479b-990a-c9c0360f883e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 678fd982505cc2bc910af9ef131f852a7f0c919a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330103"
---
# <a name="pidtagscheduleinfodisallowrecurringappts-canonical-property"></a><span data-ttu-id="3a11d-103">Propiedad canónica PidTagScheduleInfoDisallowRecurringAppts</span><span class="sxs-lookup"><span data-stu-id="3a11d-103">PidTagScheduleInfoDisallowRecurringAppts Canonical Property</span></span>

  
  
<span data-ttu-id="3a11d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a11d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a11d-105">Contiene TRUE cuando se rechaza la respuesta automática a citas periódicas.</span><span class="sxs-lookup"><span data-stu-id="3a11d-105">Contains TRUE when the automatic response to recurring appointments is decline.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3a11d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3a11d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3a11d-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span><span class="sxs-lookup"><span data-stu-id="3a11d-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span></span>  <br/> |
|<span data-ttu-id="3a11d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3a11d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3a11d-109">0x686E</span><span class="sxs-lookup"><span data-stu-id="3a11d-109">0x686E</span></span>  <br/> |
|<span data-ttu-id="3a11d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3a11d-110">Data type:</span></span>  <br/> |<span data-ttu-id="3a11d-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="3a11d-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="3a11d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3a11d-112">Area:</span></span>  <br/> |<span data-ttu-id="3a11d-113">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="3a11d-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a11d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3a11d-114">Remarks</span></span>

<span data-ttu-id="3a11d-115">Esta propiedad solo es significativa cuando el valor de **la propiedad PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) es TRUE.</span><span class="sxs-lookup"><span data-stu-id="3a11d-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="3a11d-116">La ausencia de esta propiedad indica que se deben aceptar reuniones periódicas.</span><span class="sxs-lookup"><span data-stu-id="3a11d-116">The absence of this property indicates that recurring meetings must be accepted.</span></span> <span data-ttu-id="3a11d-117">No es una propiedad obligatoria.</span><span class="sxs-lookup"><span data-stu-id="3a11d-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3a11d-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a11d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3a11d-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="3a11d-119">Protocol specifications</span></span>

<span data-ttu-id="3a11d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a11d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a11d-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="3a11d-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3a11d-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a11d-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a11d-123">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a11d-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="3a11d-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a11d-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a11d-125">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="3a11d-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3a11d-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3a11d-126">Header files</span></span>

<span data-ttu-id="3a11d-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a11d-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="3a11d-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3a11d-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="3a11d-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3a11d-129">Mapitags.h</span></span>
  
> <span data-ttu-id="3a11d-130">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="3a11d-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3a11d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a11d-131">See also</span></span>



[<span data-ttu-id="3a11d-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3a11d-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3a11d-133">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3a11d-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3a11d-134">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3a11d-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3a11d-135">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="3a11d-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

