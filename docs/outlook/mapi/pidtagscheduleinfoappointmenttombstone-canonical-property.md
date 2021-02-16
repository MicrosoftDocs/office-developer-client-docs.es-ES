---
title: Propiedad canónica PidTagScheduleInfoAppointmentTombstone
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7a7134a037aa4845ae22ab18899d27f1e50d6b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321325"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a><span data-ttu-id="ae947-103">Propiedad canónica PidTagScheduleInfoAppointmentTombstone</span><span class="sxs-lookup"><span data-stu-id="ae947-103">PidTagScheduleInfoAppointmentTombstone Canonical Property</span></span>

  
  
<span data-ttu-id="ae947-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae947-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae947-105">Contiene una lista de bloques de datos que representan reuniones rechazadas.</span><span class="sxs-lookup"><span data-stu-id="ae947-105">Contains a list of data blocks that represent meetings that have been declined.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ae947-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ae947-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ae947-107">PR_SCHDINFO_APPT_TOMBSTONE</span><span class="sxs-lookup"><span data-stu-id="ae947-107">PR_SCHDINFO_APPT_TOMBSTONE</span></span>  <br/> |
|<span data-ttu-id="ae947-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ae947-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ae947-109">0x686A</span><span class="sxs-lookup"><span data-stu-id="ae947-109">0x686A</span></span>  <br/> |
|<span data-ttu-id="ae947-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ae947-110">Data type:</span></span>  <br/> |<span data-ttu-id="ae947-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ae947-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ae947-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ae947-112">Area:</span></span>  <br/> |<span data-ttu-id="ae947-113">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="ae947-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae947-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ae947-114">Remarks</span></span>

<span data-ttu-id="ae947-115">Los bloques de datos comienzan con un encabezado de valores de 32 bits definidos como:</span><span class="sxs-lookup"><span data-stu-id="ae947-115">The data blocks begin with a header of 32 bit values defined as:</span></span>
  
|<span data-ttu-id="ae947-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ae947-116">**Value**</span></span>|<span data-ttu-id="ae947-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae947-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae947-118">Identificador</span><span class="sxs-lookup"><span data-stu-id="ae947-118">Identifier</span></span>  <br/> |<span data-ttu-id="ae947-119">Este campo debe ser el valor 0xBEDEAFCD.</span><span class="sxs-lookup"><span data-stu-id="ae947-119">This field must be the value 0xBEDEAFCD.</span></span>  <br/> |
|<span data-ttu-id="ae947-120">HeaderSize</span><span class="sxs-lookup"><span data-stu-id="ae947-120">HeaderSize</span></span>  <br/> |<span data-ttu-id="ae947-121">Este campo debe tener el valor 0x00000014.</span><span class="sxs-lookup"><span data-stu-id="ae947-121">This field must have the value 0x00000014.</span></span>  <br/> |
|<span data-ttu-id="ae947-122">Versión</span><span class="sxs-lookup"><span data-stu-id="ae947-122">Version</span></span>  <br/> |<span data-ttu-id="ae947-123">Este campo debe tener el valor 3.</span><span class="sxs-lookup"><span data-stu-id="ae947-123">This field must have the value 3.</span></span>  <br/> |
|<span data-ttu-id="ae947-124">RecordsCount</span><span class="sxs-lookup"><span data-stu-id="ae947-124">RecordsCount</span></span>  <br/> |<span data-ttu-id="ae947-125">Recuento de registros siguientes.</span><span class="sxs-lookup"><span data-stu-id="ae947-125">The count of records that follow.</span></span>  <br/> |
|<span data-ttu-id="ae947-126">RecordsSize</span><span class="sxs-lookup"><span data-stu-id="ae947-126">RecordsSize</span></span>  <br/> |<span data-ttu-id="ae947-127">Este campo debe tener el valor 0x00000014.</span><span class="sxs-lookup"><span data-stu-id="ae947-127">This field must have the value 0x00000014.</span></span>  <br/> |
   
<span data-ttu-id="ae947-128">El encabezado va seguido de **las entradas RecordsCount** de valores de 32 bits definidos como:</span><span class="sxs-lookup"><span data-stu-id="ae947-128">The header is followed by **RecordsCount** entries of 32 bit values defined as:</span></span> 
  
|<span data-ttu-id="ae947-129">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ae947-129">**Value**</span></span>|<span data-ttu-id="ae947-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae947-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae947-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="ae947-131">StartTime</span></span>  <br/> |<span data-ttu-id="ae947-132">Hora de inicio del objeto de reunión en minutos desde la medianoche del 1 de enero de 1601, UTC.</span><span class="sxs-lookup"><span data-stu-id="ae947-132">The meeting object's start time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="ae947-133">EndTime</span><span class="sxs-lookup"><span data-stu-id="ae947-133">EndTime</span></span>  <br/> |<span data-ttu-id="ae947-134">Hora de finalización del objeto de reunión en minutos desde la medianoche del 1 de enero de 1601, UTC.</span><span class="sxs-lookup"><span data-stu-id="ae947-134">The meeting object's end time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="ae947-135">GlobalObjectIdSize</span><span class="sxs-lookup"><span data-stu-id="ae947-135">GlobalObjectIdSize</span></span>  <br/> |<span data-ttu-id="ae947-136">Tamaño, en bytes, del campo GlobalObjectId.</span><span class="sxs-lookup"><span data-stu-id="ae947-136">The size, in bytes, of the GlobalObjectId field.</span></span>  <br/> |
|<span data-ttu-id="ae947-137">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="ae947-137">GlobalObjectId</span></span>  <br/> |<span data-ttu-id="ae947-138">El valor de la **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) de la reunión que representa este registro.</span><span class="sxs-lookup"><span data-stu-id="ae947-138">The value of the **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) property of the meeting this record represents.</span></span>  <br/> |
|<span data-ttu-id="ae947-139">UserName</span><span class="sxs-lookup"><span data-stu-id="ae947-139">UserName</span></span>  <br/> |<span data-ttu-id="ae947-140">Los dos primeros bytes son la longitud de la PT_STRING8 siguiente.</span><span class="sxs-lookup"><span data-stu-id="ae947-140">The first two bytes are the length of the PT_STRING8 string that follows.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ae947-141">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae947-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ae947-142">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="ae947-142">Protocol specifications</span></span>

<span data-ttu-id="ae947-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ae947-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ae947-144">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="ae947-144">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ae947-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ae947-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ae947-146">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae947-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ae947-147">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ae947-147">Header files</span></span>

<span data-ttu-id="ae947-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ae947-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="ae947-149">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ae947-149">Provides data type definitions.</span></span>
    
<span data-ttu-id="ae947-150">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ae947-150">Mapitags.h</span></span>
  
> <span data-ttu-id="ae947-151">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ae947-151">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ae947-152">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ae947-152">See also</span></span>



[<span data-ttu-id="ae947-153">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ae947-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ae947-154">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="ae947-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ae947-155">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ae947-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ae947-156">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="ae947-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

