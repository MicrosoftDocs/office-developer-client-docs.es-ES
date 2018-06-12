---
title: Propiedad canónico PidTagScheduleInfoAppointmentTombstone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAppointmentTombstone
api_type:
- COM
ms.assetid: 6b82e2ee-992f-4cbe-bdcb-e7465e556640
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 37a6d101f6ee9c04236253e143aff3a51a9208d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820214"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a><span data-ttu-id="0140e-103">Propiedad canónico PidTagScheduleInfoAppointmentTombstone</span><span class="sxs-lookup"><span data-stu-id="0140e-103">PidTagScheduleInfoAppointmentTombstone Canonical Property</span></span>

  
  
<span data-ttu-id="0140e-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0140e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0140e-105">Contiene una lista de bloques de datos que representan las reuniones que se hayan rechazado.</span><span class="sxs-lookup"><span data-stu-id="0140e-105">Contains a list of data blocks that represent meetings that have been declined.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0140e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0140e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0140e-107">PR_SCHDINFO_APPT_TOMBSTONE</span><span class="sxs-lookup"><span data-stu-id="0140e-107">PR_SCHDINFO_APPT_TOMBSTONE</span></span>  <br/> |
|<span data-ttu-id="0140e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0140e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0140e-109">0x686A</span><span class="sxs-lookup"><span data-stu-id="0140e-109">0x686A</span></span>  <br/> |
|<span data-ttu-id="0140e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0140e-110">Data type:</span></span>  <br/> |<span data-ttu-id="0140e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0140e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0140e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0140e-112">Area:</span></span>  <br/> |<span data-ttu-id="0140e-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="0140e-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0140e-114">Notas</span><span class="sxs-lookup"><span data-stu-id="0140e-114">Remarks</span></span>

<span data-ttu-id="0140e-115">Los bloques de datos comienzan con un encabezado de valores de 32 bits definido como:</span><span class="sxs-lookup"><span data-stu-id="0140e-115">The data blocks begin with a header of 32 bit values defined as:</span></span>
  
|<span data-ttu-id="0140e-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0140e-116">**Value**</span></span>|<span data-ttu-id="0140e-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0140e-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0140e-118">Identificador</span><span class="sxs-lookup"><span data-stu-id="0140e-118">Identifier</span></span>  <br/> |<span data-ttu-id="0140e-119">Este campo debe ser el valor 0xBEDEAFCD.</span><span class="sxs-lookup"><span data-stu-id="0140e-119">This field must be the value 0xBEDEAFCD.</span></span>  <br/> |
|<span data-ttu-id="0140e-120">HeaderSize</span><span class="sxs-lookup"><span data-stu-id="0140e-120">HeaderSize</span></span>  <br/> |<span data-ttu-id="0140e-121">Este campo debe tener el valor 0x00000014.</span><span class="sxs-lookup"><span data-stu-id="0140e-121">This field must have the value 0x00000014.</span></span>  <br/> |
|<span data-ttu-id="0140e-122">Versión</span><span class="sxs-lookup"><span data-stu-id="0140e-122">Version</span></span>  <br/> |<span data-ttu-id="0140e-123">Este campo debe tener el valor 3.</span><span class="sxs-lookup"><span data-stu-id="0140e-123">This field must have the value 3.</span></span>  <br/> |
|<span data-ttu-id="0140e-124">RecordsCount</span><span class="sxs-lookup"><span data-stu-id="0140e-124">RecordsCount</span></span>  <br/> |<span data-ttu-id="0140e-125">El número de registros que le siguen.</span><span class="sxs-lookup"><span data-stu-id="0140e-125">The count of records that follow.</span></span>  <br/> |
|<span data-ttu-id="0140e-126">RecordsSize</span><span class="sxs-lookup"><span data-stu-id="0140e-126">RecordsSize</span></span>  <br/> |<span data-ttu-id="0140e-127">Este campo debe tener el valor 0x00000014.</span><span class="sxs-lookup"><span data-stu-id="0140e-127">This field must have the value 0x00000014.</span></span>  <br/> |
   
<span data-ttu-id="0140e-128">El encabezado es seguido por **RecordsCount** entradas de valores de 32 bits definidos como:</span><span class="sxs-lookup"><span data-stu-id="0140e-128">The header is followed by **RecordsCount** entries of 32 bit values defined as:</span></span> 
  
|<span data-ttu-id="0140e-129">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0140e-129">**Value**</span></span>|<span data-ttu-id="0140e-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0140e-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0140e-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="0140e-131">StartTime</span></span>  <br/> |<span data-ttu-id="0140e-132">Hora de comienzo del objeto de la reunión en minutos desde la medianoche del 1 de enero de 1601, UTC.</span><span class="sxs-lookup"><span data-stu-id="0140e-132">The meeting object's start time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="0140e-133">Hora de finalización</span><span class="sxs-lookup"><span data-stu-id="0140e-133">EndTime</span></span>  <br/> |<span data-ttu-id="0140e-134">Hora de finalización del objeto de la reunión en minutos desde la medianoche del 1 de enero de 1601, UTC.</span><span class="sxs-lookup"><span data-stu-id="0140e-134">The meeting object's end time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="0140e-135">GlobalObjectIdSize</span><span class="sxs-lookup"><span data-stu-id="0140e-135">GlobalObjectIdSize</span></span>  <br/> |<span data-ttu-id="0140e-136">El tamaño, en bytes, del campo GlobalObjectId.</span><span class="sxs-lookup"><span data-stu-id="0140e-136">The size, in bytes, of the GlobalObjectId field.</span></span>  <br/> |
|<span data-ttu-id="0140e-137">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="0140e-137">GlobalObjectId</span></span>  <br/> |<span data-ttu-id="0140e-138">Representa el valor de la propiedad **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) de la reunión este registro.</span><span class="sxs-lookup"><span data-stu-id="0140e-138">The value of the **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) property of the meeting this record represents.</span></span>  <br/> |
|<span data-ttu-id="0140e-139">UserName</span><span class="sxs-lookup"><span data-stu-id="0140e-139">UserName</span></span>  <br/> |<span data-ttu-id="0140e-140">Los dos primeros bytes son la longitud de la cadena de PT_STRING8 que sigue.</span><span class="sxs-lookup"><span data-stu-id="0140e-140">The first two bytes are the length of the PT_STRING8 string that follows.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0140e-141">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0140e-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0140e-142">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0140e-142">Protocol specifications</span></span>

<span data-ttu-id="0140e-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0140e-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0140e-144">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0140e-144">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0140e-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0140e-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0140e-146">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="0140e-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0140e-147">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0140e-147">Header files</span></span>

<span data-ttu-id="0140e-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0140e-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="0140e-149">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0140e-149">Provides data type definitions.</span></span>
    
<span data-ttu-id="0140e-150">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0140e-150">Mapitags.h</span></span>
  
> <span data-ttu-id="0140e-151">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0140e-151">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0140e-152">Ver también</span><span class="sxs-lookup"><span data-stu-id="0140e-152">See also</span></span>



[<span data-ttu-id="0140e-153">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0140e-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0140e-154">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0140e-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0140e-155">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="0140e-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0140e-156">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0140e-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

