---
title: Propiedad canónica PidLidAppointmentDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentDuration
api_type:
- COM
ms.assetid: 92c07a81-9dec-4118-af1f-02ecad340f07
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0d124bd3aa4350863351284a9e4b19ca4533e382
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818486"
---
# <a name="pidlidappointmentduration-canonical-property"></a><span data-ttu-id="97016-103">Propiedad canónica PidLidAppointmentDuration</span><span class="sxs-lookup"><span data-stu-id="97016-103">PidLidAppointmentDuration Canonical Property</span></span>

  
  
<span data-ttu-id="97016-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="97016-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="97016-105">Representa el período de tiempo, en minutos, cuando se programa una cita.</span><span class="sxs-lookup"><span data-stu-id="97016-105">Represents the length of time, in minutes, when an appointment is scheduled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97016-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="97016-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="97016-107">dispidApptDuration</span><span class="sxs-lookup"><span data-stu-id="97016-107">dispidApptDuration</span></span>  <br/> |
|<span data-ttu-id="97016-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="97016-108">Property set:</span></span>  <br/> |<span data-ttu-id="97016-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="97016-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="97016-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="97016-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="97016-111">0x00008213</span><span class="sxs-lookup"><span data-stu-id="97016-111">0x00008213</span></span>  <br/> |
|<span data-ttu-id="97016-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="97016-112">Data type:</span></span>  <br/> |<span data-ttu-id="97016-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="97016-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="97016-114">Área:</span><span class="sxs-lookup"><span data-stu-id="97016-114">Area:</span></span>  <br/> |<span data-ttu-id="97016-115">Calendario</span><span class="sxs-lookup"><span data-stu-id="97016-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97016-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="97016-116">Remarks</span></span>

<span data-ttu-id="97016-117">El valor debe ser el número de minutos entre el valor de la **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) y las propiedades de **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="97016-117">The value must be the number of minutes between the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) and the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="97016-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="97016-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="97016-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="97016-119">Protocol specifications</span></span>

<span data-ttu-id="97016-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97016-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97016-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="97016-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="97016-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97016-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97016-123">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="97016-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="97016-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="97016-124">Header files</span></span>

<span data-ttu-id="97016-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="97016-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="97016-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="97016-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97016-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="97016-127">See also</span></span>



[<span data-ttu-id="97016-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="97016-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="97016-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="97016-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="97016-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="97016-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="97016-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="97016-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

