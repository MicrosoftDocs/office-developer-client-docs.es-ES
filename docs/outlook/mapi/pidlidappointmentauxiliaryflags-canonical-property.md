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
ms.openlocfilehash: 4414ae866dece0654131d1575fe699676892709f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345433"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a><span data-ttu-id="e8531-103">Propiedad canónica PidLidAppointmentAuxiliaryFlags</span><span class="sxs-lookup"><span data-stu-id="e8531-103">PidLidAppointmentAuxiliaryFlags Canonical Property</span></span>

  
  
<span data-ttu-id="e8531-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8531-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8531-105">Especifica un campo de bits que describe el estado auxiliar del objeto.</span><span class="sxs-lookup"><span data-stu-id="e8531-105">Specifies a bit field that describes the auxiliary state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e8531-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e8531-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e8531-107">dispidApptAuxFlags</span><span class="sxs-lookup"><span data-stu-id="e8531-107">dispidApptAuxFlags</span></span>  <br/> |
|<span data-ttu-id="e8531-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e8531-108">Property set:</span></span>  <br/> |<span data-ttu-id="e8531-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="e8531-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="e8531-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="e8531-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e8531-111">0x00008207</span><span class="sxs-lookup"><span data-stu-id="e8531-111">0x00008207</span></span>  <br/> |
|<span data-ttu-id="e8531-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e8531-112">Data type:</span></span>  <br/> |<span data-ttu-id="e8531-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e8531-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e8531-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e8531-114">Area:</span></span>  <br/> |<span data-ttu-id="e8531-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="e8531-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8531-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8531-116">Remarks</span></span>

<span data-ttu-id="e8531-117">Esta propiedad no es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="e8531-117">This property is not required.</span></span> <span data-ttu-id="e8531-118">A continuación se muestran las marcas individuales que se pueden establecer.</span><span class="sxs-lookup"><span data-stu-id="e8531-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="e8531-119">C (auxApptFlagCopied, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="e8531-119">C (auxApptFlagCopied, 0x00000001)</span></span>
  
> <span data-ttu-id="e8531-120">Esta marca indica que el objeto de calendario se copió de otra carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="e8531-120">This flag indicates that the calendar object was copied from another calendar folder.</span></span>
    
<span data-ttu-id="e8531-121">R (auxApptFlagForceMtgResponse, 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="e8531-121">R (auxApptFlagForceMtgResponse, 0x00000002)</span></span>
  
> <span data-ttu-id="e8531-122">Esta marca en una convocatoria de reunión indica que el cliente o el servidor debe enviar una respuesta de reunión de vuelta al organizador cuando se elige una respuesta.</span><span class="sxs-lookup"><span data-stu-id="e8531-122">This flag on a meeting request indicates that the client or server should send a meeting response back to the organizer when a response is chosen.</span></span>
    
<span data-ttu-id="e8531-123">F (auxApptFlagForwarded, 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="e8531-123">F (auxApptFlagForwarded, 0x00000004)</span></span>
  
> <span data-ttu-id="e8531-124">Esta marca en una convocatoria de reunión indica que se reenvió (incluso si el organizador lo reenvió), en lugar de ser una invitación del organizador.</span><span class="sxs-lookup"><span data-stu-id="e8531-124">This flag on a meeting request indicates that it was forwarded (including being forwarded by the organizer), rather than being an invitation from the organizer.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="e8531-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8531-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e8531-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e8531-126">Protocol specifications</span></span>

<span data-ttu-id="e8531-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8531-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8531-128">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e8531-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e8531-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8531-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8531-130">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="e8531-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e8531-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e8531-131">Header files</span></span>

<span data-ttu-id="e8531-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e8531-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="e8531-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e8531-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e8531-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8531-134">See also</span></span>



[<span data-ttu-id="e8531-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e8531-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e8531-136">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="e8531-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e8531-137">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e8531-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e8531-138">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="e8531-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

