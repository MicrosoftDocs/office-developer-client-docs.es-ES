---
title: Propiedad canónica PidLidAppointmentReplyTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentReplyTime
api_type:
- COM
ms.assetid: 80a2608b-fc44-455a-86be-d6235caba99e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ba79498569c544d1b0ee22e968477d5b68812c09
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398279"
---
# <a name="pidlidappointmentreplytime-canonical-property"></a><span data-ttu-id="6646b-103">Propiedad canónica PidLidAppointmentReplyTime</span><span class="sxs-lookup"><span data-stu-id="6646b-103">PidLidAppointmentReplyTime Canonical Property</span></span>

  
  
<span data-ttu-id="6646b-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6646b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6646b-105">Especifica la fecha y la hora cuando el asistente ha respondido a una convocatoria de reunión recibida o actualización de la reunión.</span><span class="sxs-lookup"><span data-stu-id="6646b-105">Specifies the date and time when the attendee responded to a received meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6646b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6646b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6646b-107">dispidApptReplyTime</span><span class="sxs-lookup"><span data-stu-id="6646b-107">dispidApptReplyTime</span></span>  <br/> |
|<span data-ttu-id="6646b-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="6646b-108">Property set:</span></span>  <br/> |<span data-ttu-id="6646b-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="6646b-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="6646b-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="6646b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6646b-111">0x00008220</span><span class="sxs-lookup"><span data-stu-id="6646b-111">0x00008220</span></span>  <br/> |
|<span data-ttu-id="6646b-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6646b-112">Data type:</span></span>  <br/> |<span data-ttu-id="6646b-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="6646b-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="6646b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="6646b-114">Area:</span></span>  <br/> |<span data-ttu-id="6646b-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="6646b-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6646b-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6646b-116">Remarks</span></span>

<span data-ttu-id="6646b-117">El valor debe especificarse en hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="6646b-117">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6646b-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6646b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6646b-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="6646b-119">Protocol specifications</span></span>

<span data-ttu-id="6646b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6646b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6646b-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6646b-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6646b-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6646b-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6646b-123">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="6646b-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6646b-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6646b-124">Header files</span></span>

<span data-ttu-id="6646b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6646b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="6646b-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6646b-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6646b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="6646b-127">See also</span></span>



[<span data-ttu-id="6646b-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6646b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6646b-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="6646b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6646b-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6646b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6646b-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="6646b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

