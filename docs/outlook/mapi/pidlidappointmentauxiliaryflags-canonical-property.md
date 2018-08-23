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
ms.openlocfilehash: 5e05144beeac8318b8c28153461742a491698996
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576634"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a><span data-ttu-id="cb764-103">Propiedad canónica PidLidAppointmentAuxiliaryFlags</span><span class="sxs-lookup"><span data-stu-id="cb764-103">PidLidAppointmentAuxiliaryFlags Canonical Property</span></span>

  
  
<span data-ttu-id="cb764-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb764-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb764-105">Especifica un campo de bits que describe el estado del objeto auxiliar.</span><span class="sxs-lookup"><span data-stu-id="cb764-105">Specifies a bit field that describes the auxiliary state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cb764-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cb764-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb764-107">dispidApptAuxFlags</span><span class="sxs-lookup"><span data-stu-id="cb764-107">dispidApptAuxFlags</span></span>  <br/> |
|<span data-ttu-id="cb764-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="cb764-108">Property set:</span></span>  <br/> |<span data-ttu-id="cb764-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="cb764-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="cb764-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="cb764-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cb764-111">0x00008207</span><span class="sxs-lookup"><span data-stu-id="cb764-111">0x00008207</span></span>  <br/> |
|<span data-ttu-id="cb764-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cb764-112">Data type:</span></span>  <br/> |<span data-ttu-id="cb764-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cb764-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cb764-114">Área:</span><span class="sxs-lookup"><span data-stu-id="cb764-114">Area:</span></span>  <br/> |<span data-ttu-id="cb764-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="cb764-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb764-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb764-116">Remarks</span></span>

<span data-ttu-id="cb764-117">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="cb764-117">This property is not required.</span></span> <span data-ttu-id="cb764-118">A continuación se muestran los indicadores individuales que se pueden establecer.</span><span class="sxs-lookup"><span data-stu-id="cb764-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="cb764-119">C (auxApptFlagCopied, 0 x 00000001)</span><span class="sxs-lookup"><span data-stu-id="cb764-119">C (auxApptFlagCopied, 0x00000001)</span></span>
  
> <span data-ttu-id="cb764-120">Esta marca indica que el objeto de calendario se copió desde otra carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="cb764-120">This flag indicates that the calendar object was copied from another calendar folder.</span></span>
    
<span data-ttu-id="cb764-121">R (auxApptFlagForceMtgResponse, 0 x 00000002)</span><span class="sxs-lookup"><span data-stu-id="cb764-121">R (auxApptFlagForceMtgResponse, 0x00000002)</span></span>
  
> <span data-ttu-id="cb764-122">Esta marca en una convocatoria de reunión indica que el cliente o el servidor debe enviar una respuesta de reunión al organizador cuando se elige una respuesta.</span><span class="sxs-lookup"><span data-stu-id="cb764-122">This flag on a meeting request indicates that the client or server should send a meeting response back to the organizer when a response is chosen.</span></span>
    
<span data-ttu-id="cb764-123">F (auxApptFlagForwarded, 0 x 00000004)</span><span class="sxs-lookup"><span data-stu-id="cb764-123">F (auxApptFlagForwarded, 0x00000004)</span></span>
  
> <span data-ttu-id="cb764-124">Esta marca en una convocatoria de reunión indica que se reenvió (incluidos se reenvíen por el organizador), en lugar de ser una invitación del organizador.</span><span class="sxs-lookup"><span data-stu-id="cb764-124">This flag on a meeting request indicates that it was forwarded (including being forwarded by the organizer), rather than being an invitation from the organizer.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="cb764-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb764-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cb764-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="cb764-126">Protocol specifications</span></span>

<span data-ttu-id="cb764-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb764-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb764-128">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="cb764-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cb764-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb764-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb764-130">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="cb764-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cb764-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cb764-131">Header files</span></span>

<span data-ttu-id="cb764-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cb764-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="cb764-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cb764-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb764-134">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="cb764-134">See also</span></span>



[<span data-ttu-id="cb764-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cb764-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cb764-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="cb764-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cb764-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cb764-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cb764-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="cb764-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

