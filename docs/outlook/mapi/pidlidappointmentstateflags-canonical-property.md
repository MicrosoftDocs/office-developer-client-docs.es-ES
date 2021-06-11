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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345363"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a><span data-ttu-id="4949c-103">Propiedad canónica PidLidAppointmentStateFlags</span><span class="sxs-lookup"><span data-stu-id="4949c-103">PidLidAppointmentStateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="4949c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4949c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4949c-105">Especifica un campo de bits que describe el estado del objeto.</span><span class="sxs-lookup"><span data-stu-id="4949c-105">Specifies a bit field that describes the state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4949c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4949c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4949c-107">dispidApptStateFlags</span><span class="sxs-lookup"><span data-stu-id="4949c-107">dispidApptStateFlags</span></span>  <br/> |
|<span data-ttu-id="4949c-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="4949c-108">Property set:</span></span>  <br/> |<span data-ttu-id="4949c-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="4949c-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="4949c-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="4949c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4949c-111">0x00008217</span><span class="sxs-lookup"><span data-stu-id="4949c-111">0x00008217</span></span>  <br/> |
|<span data-ttu-id="4949c-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4949c-112">Data type:</span></span>  <br/> |<span data-ttu-id="4949c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4949c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4949c-114">Área:</span><span class="sxs-lookup"><span data-stu-id="4949c-114">Area:</span></span>  <br/> |<span data-ttu-id="4949c-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="4949c-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4949c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4949c-116">Remarks</span></span>

<span data-ttu-id="4949c-117">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="4949c-117">This property is not required.</span></span> <span data-ttu-id="4949c-118">A continuación se muestran las marcas individuales que se pueden establecer.</span><span class="sxs-lookup"><span data-stu-id="4949c-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="4949c-119">M (asfMeeting, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="4949c-119">M (asfMeeting, 0x00000001)</span></span>
  
> <span data-ttu-id="4949c-120">Esta marca indica que el objeto es un objeto de reunión o un objeto relacionado con la reunión.</span><span class="sxs-lookup"><span data-stu-id="4949c-120">This flag indicates that the object is a meeting object or a meeting-related object.</span></span>
    
<span data-ttu-id="4949c-121">R (asfReceived, 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="4949c-121">R (asfReceived, 0x00000002)</span></span>
  
> <span data-ttu-id="4949c-122">Esta marca indica que el objeto representado se recibió de otra persona.</span><span class="sxs-lookup"><span data-stu-id="4949c-122">This flag indicates that the represented object was received from someone else.</span></span>
    
<span data-ttu-id="4949c-123">C (asfCanceled, 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="4949c-123">C (asfCanceled, 0x00000004)</span></span>
  
> <span data-ttu-id="4949c-124">Esta marca indica que se ha cancelado el objeto de reunión representado por el objeto.</span><span class="sxs-lookup"><span data-stu-id="4949c-124">This flag indicates that the meeting object represented by the object has been canceled.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="4949c-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4949c-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4949c-126">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="4949c-126">Protocol specifications</span></span>

<span data-ttu-id="4949c-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4949c-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4949c-128">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="4949c-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4949c-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4949c-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4949c-130">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="4949c-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4949c-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4949c-131">Header files</span></span>

<span data-ttu-id="4949c-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4949c-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="4949c-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4949c-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4949c-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="4949c-134">See also</span></span>



[<span data-ttu-id="4949c-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4949c-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4949c-136">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="4949c-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4949c-137">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4949c-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4949c-138">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="4949c-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

