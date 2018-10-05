---
title: Propiedad canónica PidLidAppointmentProposedDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentProposedDuration
api_type:
- COM
ms.assetid: 37806778-a19a-4905-a845-525d3912bf9e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 56a652e630af70d4cfde12995951a352a1aa97e3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390622"
---
# <a name="pidlidappointmentproposedduration-canonical-property"></a><span data-ttu-id="190de-103">Propiedad canónica PidLidAppointmentProposedDuration</span><span class="sxs-lookup"><span data-stu-id="190de-103">PidLidAppointmentProposedDuration Canonical Property</span></span>

  
  
<span data-ttu-id="190de-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="190de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="190de-105">Indica el valor propuesto para la propiedad **dispidApptDuration** ([PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)) de una propuesta de contador.</span><span class="sxs-lookup"><span data-stu-id="190de-105">Indicates the proposed value for the **dispidApptDuration** ([PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)) property for a counter proposal.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="190de-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="190de-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="190de-107">dispidApptProposedDuration</span><span class="sxs-lookup"><span data-stu-id="190de-107">dispidApptProposedDuration</span></span>  <br/> |
|<span data-ttu-id="190de-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="190de-108">Property set:</span></span>  <br/> |<span data-ttu-id="190de-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="190de-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="190de-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="190de-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="190de-111">0x00008256</span><span class="sxs-lookup"><span data-stu-id="190de-111">0x00008256</span></span>  <br/> |
|<span data-ttu-id="190de-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="190de-112">Data type:</span></span>  <br/> |<span data-ttu-id="190de-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="190de-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="190de-114">Área:</span><span class="sxs-lookup"><span data-stu-id="190de-114">Area:</span></span>  <br/> |<span data-ttu-id="190de-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="190de-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="190de-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="190de-116">Remarks</span></span>

<span data-ttu-id="190de-117">Si se establece, debe ser igual que el número de minutos entre las propiedades de **dispidApptProposedEndWhole** ([PidLidAppointmentProposedEndWhole](pidlidappointmentproposedendwhole-canonical-property.md)) y **dispidApptProposedStartWhole** ([PidLidAppointmentProposedStartWhole](pidlidappointmentproposedstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="190de-117">If set, it must be equal to the number of minutes between the **dispidApptProposedStartWhole** ([PidLidAppointmentProposedStartWhole](pidlidappointmentproposedstartwhole-canonical-property.md)) and **dispidApptProposedEndWhole** ([PidLidAppointmentProposedEndWhole](pidlidappointmentproposedendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="190de-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="190de-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="190de-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="190de-119">Protocol specifications</span></span>

<span data-ttu-id="190de-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="190de-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="190de-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="190de-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="190de-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="190de-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="190de-123">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="190de-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="190de-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="190de-124">Header files</span></span>

<span data-ttu-id="190de-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="190de-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="190de-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="190de-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="190de-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="190de-127">See also</span></span>



[<span data-ttu-id="190de-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="190de-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="190de-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="190de-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="190de-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="190de-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="190de-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="190de-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

