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
ms.openlocfilehash: 293eb489a1e926f0e60e823a536dacf6f409e353
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818559"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a><span data-ttu-id="5c0eb-103">Propiedad canónica PidLidAppointmentStateFlags</span><span class="sxs-lookup"><span data-stu-id="5c0eb-103">PidLidAppointmentStateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="5c0eb-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5c0eb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5c0eb-105">Especifica un campo de bits que describe el estado del objeto.</span><span class="sxs-lookup"><span data-stu-id="5c0eb-105">Specifies a bit field that describes the state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5c0eb-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5c0eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c0eb-107">dispidApptStateFlags</span><span class="sxs-lookup"><span data-stu-id="5c0eb-107">dispidApptStateFlags</span></span>  <br/> |
|<span data-ttu-id="5c0eb-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="5c0eb-108">Property set:</span></span>  <br/> |<span data-ttu-id="5c0eb-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="5c0eb-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="5c0eb-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="5c0eb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5c0eb-111">0x00008217</span><span class="sxs-lookup"><span data-stu-id="5c0eb-111">0x00008217</span></span>  <br/> |
|<span data-ttu-id="5c0eb-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5c0eb-112">Data type:</span></span>  <br/> |<span data-ttu-id="5c0eb-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5c0eb-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5c0eb-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5c0eb-114">Area:</span></span>  <br/> |<span data-ttu-id="5c0eb-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="5c0eb-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c0eb-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5c0eb-116">Remarks</span></span>

<span data-ttu-id="5c0eb-117">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="5c0eb-117">This property is not required.</span></span> <span data-ttu-id="5c0eb-118">A continuación se muestran los indicadores individuales que se pueden establecer.</span><span class="sxs-lookup"><span data-stu-id="5c0eb-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="5c0eb-119">M (asfMeeting, 0 x 00000001)</span><span class="sxs-lookup"><span data-stu-id="5c0eb-119">M (asfMeeting, 0x00000001)</span></span>
  
> <span data-ttu-id="5c0eb-120">Esta marca indica que el objeto es un objeto de la reunión o un objeto relacionado con la reunión.</span><span class="sxs-lookup"><span data-stu-id="5c0eb-120">This flag indicates that the object is a meeting object or a meeting-related object.</span></span>
    
<span data-ttu-id="5c0eb-121">R (asfReceived, 0 x 00000002)</span><span class="sxs-lookup"><span data-stu-id="5c0eb-121">R (asfReceived, 0x00000002)</span></span>
  
> <span data-ttu-id="5c0eb-122">Esta marca indica que se ha recibido el objeto representado de otra persona.</span><span class="sxs-lookup"><span data-stu-id="5c0eb-122">This flag indicates that the represented object was received from someone else.</span></span>
    
<span data-ttu-id="5c0eb-123">C (asfCanceled, 0 x 00000004)</span><span class="sxs-lookup"><span data-stu-id="5c0eb-123">C (asfCanceled, 0x00000004)</span></span>
  
> <span data-ttu-id="5c0eb-124">Esta marca indica que se ha cancelado el objeto de reunión representado por el objeto.</span><span class="sxs-lookup"><span data-stu-id="5c0eb-124">This flag indicates that the meeting object represented by the object has been canceled.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="5c0eb-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c0eb-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5c0eb-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5c0eb-126">Protocol specifications</span></span>

<span data-ttu-id="5c0eb-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c0eb-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c0eb-128">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5c0eb-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5c0eb-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c0eb-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c0eb-130">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c0eb-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5c0eb-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5c0eb-131">Header files</span></span>

<span data-ttu-id="5c0eb-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c0eb-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c0eb-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5c0eb-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c0eb-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c0eb-134">See also</span></span>



[<span data-ttu-id="5c0eb-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5c0eb-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5c0eb-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5c0eb-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5c0eb-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5c0eb-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5c0eb-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5c0eb-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

