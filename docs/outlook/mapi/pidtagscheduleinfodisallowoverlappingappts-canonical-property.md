---
title: Propiedad canónica PidTagScheduleInfoDisallowOverlappingAppts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowOverlappingAppts
api_type:
- COM
ms.assetid: 27978a09-daf7-4a50-927a-96d9c4a97d02
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5ead258c056ec2204ddab92e9b99e1b17fe98092
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330089"
---
# <a name="pidtagscheduleinfodisallowoverlappingappts-canonical-property"></a><span data-ttu-id="c13ff-103">Propiedad canónica PidTagScheduleInfoDisallowOverlappingAppts</span><span class="sxs-lookup"><span data-stu-id="c13ff-103">PidTagScheduleInfoDisallowOverlappingAppts Canonical Property</span></span>

  
  
<span data-ttu-id="c13ff-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c13ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c13ff-105">Contiene TRUE si no se pueden superponer citas.</span><span class="sxs-lookup"><span data-stu-id="c13ff-105">Contains TRUE if overlapping appointments are disallowed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c13ff-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c13ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c13ff-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span><span class="sxs-lookup"><span data-stu-id="c13ff-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span></span>  <br/> |
|<span data-ttu-id="c13ff-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c13ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c13ff-109">0x686F</span><span class="sxs-lookup"><span data-stu-id="c13ff-109">0x686F</span></span>  <br/> |
|<span data-ttu-id="c13ff-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c13ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="c13ff-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c13ff-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c13ff-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c13ff-112">Area:</span></span>  <br/> |<span data-ttu-id="c13ff-113">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="c13ff-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c13ff-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c13ff-114">Remarks</span></span>

<span data-ttu-id="c13ff-115">Esta propiedad solo es significativa cuando el valor de **la propiedad PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) es TRUE.</span><span class="sxs-lookup"><span data-stu-id="c13ff-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="c13ff-116">Un valor TRUE indica que, al responder automáticamente a las solicitudes de reunión, un cliente o servidor debe rechazar instancias que se superponen a eventos previamente programados.</span><span class="sxs-lookup"><span data-stu-id="c13ff-116">A value of TRUE indicates that when automatically responding to meeting requests, a client or server must decline instances that overlap previously scheduled events.</span></span> <span data-ttu-id="c13ff-117">Un valor FALSE o la ausencia de esta propiedad indica que se deben aceptar instancias superpuestas.</span><span class="sxs-lookup"><span data-stu-id="c13ff-117">A value of FALSE or the absence of this property indicates that overlapping instances must be accepted.</span></span> <span data-ttu-id="c13ff-118">Esta propiedad no es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="c13ff-118">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c13ff-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c13ff-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c13ff-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="c13ff-120">Protocol specifications</span></span>

<span data-ttu-id="c13ff-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c13ff-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c13ff-122">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="c13ff-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c13ff-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c13ff-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c13ff-124">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="c13ff-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="c13ff-125">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c13ff-125">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c13ff-126">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="c13ff-126">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c13ff-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c13ff-127">Header files</span></span>

<span data-ttu-id="c13ff-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c13ff-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="c13ff-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c13ff-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="c13ff-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c13ff-130">Mapitags.h</span></span>
  
> <span data-ttu-id="c13ff-131">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c13ff-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c13ff-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c13ff-132">See also</span></span>



[<span data-ttu-id="c13ff-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c13ff-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c13ff-134">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="c13ff-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c13ff-135">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c13ff-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c13ff-136">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="c13ff-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

