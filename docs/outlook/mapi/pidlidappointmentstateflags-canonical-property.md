---
title: Propiedad canónica PidLidAppointmentStateFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStateFlags
api_type:
- COM
ms.assetid: 1e5f0f83-c40b-4b3a-8492-61d1b53b1e3c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e365c78ea6457e7da79e3d1c749baa922a01acbb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391335"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a><span data-ttu-id="78727-103">Propiedad canónica PidLidAppointmentStateFlags</span><span class="sxs-lookup"><span data-stu-id="78727-103">PidLidAppointmentStateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="78727-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78727-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78727-105">Especifica un campo de bits que describe el estado del objeto.</span><span class="sxs-lookup"><span data-stu-id="78727-105">Specifies a bit field that describes the state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78727-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="78727-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="78727-107">dispidApptStateFlags</span><span class="sxs-lookup"><span data-stu-id="78727-107">dispidApptStateFlags</span></span>  <br/> |
|<span data-ttu-id="78727-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="78727-108">Property set:</span></span>  <br/> |<span data-ttu-id="78727-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="78727-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="78727-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="78727-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="78727-111">0x00008217</span><span class="sxs-lookup"><span data-stu-id="78727-111">0x00008217</span></span>  <br/> |
|<span data-ttu-id="78727-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="78727-112">Data type:</span></span>  <br/> |<span data-ttu-id="78727-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="78727-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="78727-114">Área:</span><span class="sxs-lookup"><span data-stu-id="78727-114">Area:</span></span>  <br/> |<span data-ttu-id="78727-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="78727-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78727-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="78727-116">Remarks</span></span>

<span data-ttu-id="78727-117">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="78727-117">This property is not required.</span></span> <span data-ttu-id="78727-118">A continuación se muestran los indicadores individuales que se pueden establecer.</span><span class="sxs-lookup"><span data-stu-id="78727-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="78727-119">M (asfMeeting, 0 x 00000001)</span><span class="sxs-lookup"><span data-stu-id="78727-119">M (asfMeeting, 0x00000001)</span></span>
  
> <span data-ttu-id="78727-120">Esta marca indica que el objeto es un objeto de la reunión o un objeto relacionado con la reunión.</span><span class="sxs-lookup"><span data-stu-id="78727-120">This flag indicates that the object is a meeting object or a meeting-related object.</span></span>
    
<span data-ttu-id="78727-121">R (asfReceived, 0 x 00000002)</span><span class="sxs-lookup"><span data-stu-id="78727-121">R (asfReceived, 0x00000002)</span></span>
  
> <span data-ttu-id="78727-122">Esta marca indica que se ha recibido el objeto representado de otra persona.</span><span class="sxs-lookup"><span data-stu-id="78727-122">This flag indicates that the represented object was received from someone else.</span></span>
    
<span data-ttu-id="78727-123">C (asfCanceled, 0 x 00000004)</span><span class="sxs-lookup"><span data-stu-id="78727-123">C (asfCanceled, 0x00000004)</span></span>
  
> <span data-ttu-id="78727-124">Esta marca indica que se ha cancelado el objeto de reunión representado por el objeto.</span><span class="sxs-lookup"><span data-stu-id="78727-124">This flag indicates that the meeting object represented by the object has been canceled.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="78727-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="78727-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="78727-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="78727-126">Protocol specifications</span></span>

<span data-ttu-id="78727-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78727-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78727-128">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="78727-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="78727-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78727-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78727-130">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="78727-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="78727-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="78727-131">Header files</span></span>

<span data-ttu-id="78727-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="78727-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="78727-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="78727-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="78727-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="78727-134">See also</span></span>



[<span data-ttu-id="78727-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="78727-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="78727-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="78727-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="78727-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="78727-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="78727-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="78727-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

