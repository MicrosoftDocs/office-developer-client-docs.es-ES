---
title: Propiedad canónica PidLidAppointmentAuxiliaryFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentAuxiliaryFlags
api_type:
- COM
ms.assetid: 56c64e23-4a99-4f80-ba06-dfae2a5fe961
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cac9c735403e6cb65dfe3111a2246a8387339339
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818469"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a><span data-ttu-id="a085d-103">Propiedad canónica PidLidAppointmentAuxiliaryFlags</span><span class="sxs-lookup"><span data-stu-id="a085d-103">PidLidAppointmentAuxiliaryFlags Canonical Property</span></span>

  
  
<span data-ttu-id="a085d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a085d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a085d-105">Especifica un campo de bits que describe el estado del objeto auxiliar.</span><span class="sxs-lookup"><span data-stu-id="a085d-105">Specifies a bit field that describes the auxiliary state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a085d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a085d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a085d-107">dispidApptAuxFlags</span><span class="sxs-lookup"><span data-stu-id="a085d-107">dispidApptAuxFlags</span></span>  <br/> |
|<span data-ttu-id="a085d-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="a085d-108">Property set:</span></span>  <br/> |<span data-ttu-id="a085d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a085d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a085d-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="a085d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a085d-111">0x00008207</span><span class="sxs-lookup"><span data-stu-id="a085d-111">0x00008207</span></span>  <br/> |
|<span data-ttu-id="a085d-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a085d-112">Data type:</span></span>  <br/> |<span data-ttu-id="a085d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a085d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a085d-114">Área:</span><span class="sxs-lookup"><span data-stu-id="a085d-114">Area:</span></span>  <br/> |<span data-ttu-id="a085d-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="a085d-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a085d-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a085d-116">Remarks</span></span>

<span data-ttu-id="a085d-117">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="a085d-117">This property is not required.</span></span> <span data-ttu-id="a085d-118">A continuación se muestran los indicadores individuales que se pueden establecer.</span><span class="sxs-lookup"><span data-stu-id="a085d-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="a085d-119">C (auxApptFlagCopied, 0 x 00000001)</span><span class="sxs-lookup"><span data-stu-id="a085d-119">C (auxApptFlagCopied, 0x00000001)</span></span>
  
> <span data-ttu-id="a085d-120">Esta marca indica que el objeto de calendario se copió desde otra carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="a085d-120">This flag indicates that the calendar object was copied from another calendar folder.</span></span>
    
<span data-ttu-id="a085d-121">R (auxApptFlagForceMtgResponse, 0 x 00000002)</span><span class="sxs-lookup"><span data-stu-id="a085d-121">R (auxApptFlagForceMtgResponse, 0x00000002)</span></span>
  
> <span data-ttu-id="a085d-122">Esta marca en una convocatoria de reunión indica que el cliente o el servidor debe enviar una respuesta de reunión al organizador cuando se elige una respuesta.</span><span class="sxs-lookup"><span data-stu-id="a085d-122">This flag on a meeting request indicates that the client or server should send a meeting response back to the organizer when a response is chosen.</span></span>
    
<span data-ttu-id="a085d-123">F (auxApptFlagForwarded, 0 x 00000004)</span><span class="sxs-lookup"><span data-stu-id="a085d-123">F (auxApptFlagForwarded, 0x00000004)</span></span>
  
> <span data-ttu-id="a085d-124">Esta marca en una convocatoria de reunión indica que se reenvió (incluidos se reenvíen por el organizador), en lugar de ser una invitación del organizador.</span><span class="sxs-lookup"><span data-stu-id="a085d-124">This flag on a meeting request indicates that it was forwarded (including being forwarded by the organizer), rather than being an invitation from the organizer.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="a085d-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a085d-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a085d-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a085d-126">Protocol specifications</span></span>

<span data-ttu-id="a085d-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a085d-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a085d-128">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a085d-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a085d-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a085d-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a085d-130">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a085d-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a085d-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a085d-131">Header files</span></span>

<span data-ttu-id="a085d-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a085d-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="a085d-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a085d-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a085d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="a085d-134">See also</span></span>



[<span data-ttu-id="a085d-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a085d-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a085d-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a085d-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a085d-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a085d-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a085d-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="a085d-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

