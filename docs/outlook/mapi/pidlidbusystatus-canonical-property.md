---
title: Propiedad canónica PidLidBusyStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusyStatus
api_type:
- COM
ms.assetid: 50c91fe6-2a61-4348-a16d-fd5c501b0715
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cb73a0e09436177b8b53a05588508886ee28a0a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342031"
---
# <a name="pidlidbusystatus-canonical-property"></a><span data-ttu-id="c1c93-103">Propiedad canónica PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="c1c93-103">PidLidBusyStatus Canonical Property</span></span>

  
  
<span data-ttu-id="c1c93-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1c93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1c93-105">Representa la disponibilidad del usuario para una cita.</span><span class="sxs-lookup"><span data-stu-id="c1c93-105">Represents the user's availability for an appointment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c1c93-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c1c93-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c1c93-107">dispidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="c1c93-107">dispidBusyStatus</span></span>  <br/> |
|<span data-ttu-id="c1c93-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="c1c93-108">Property set:</span></span>  <br/> |<span data-ttu-id="c1c93-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="c1c93-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="c1c93-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="c1c93-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c1c93-111">0x00008205</span><span class="sxs-lookup"><span data-stu-id="c1c93-111">0x00008205</span></span>  <br/> |
|<span data-ttu-id="c1c93-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c1c93-112">Data type:</span></span>  <br/> |<span data-ttu-id="c1c93-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c1c93-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c1c93-114">Área:</span><span class="sxs-lookup"><span data-stu-id="c1c93-114">Area:</span></span>  <br/> |<span data-ttu-id="c1c93-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="c1c93-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1c93-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1c93-116">Remarks</span></span>

<span data-ttu-id="c1c93-117">Esta propiedad especifica la disponibilidad de un usuario para el evento descrito por el objeto y debe ser uno de los valores especificados a continuación.</span><span class="sxs-lookup"><span data-stu-id="c1c93-117">This property specifies the availability of a user for the event described by the object and must be one of the values specified below.</span></span>
  
|<span data-ttu-id="c1c93-118">**Value**</span><span class="sxs-lookup"><span data-stu-id="c1c93-118">**Value**</span></span>|<span data-ttu-id="c1c93-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1c93-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1c93-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1c93-120">0x00000000</span></span>  <br/> |<span data-ttu-id="c1c93-121">El usuario está disponible.</span><span class="sxs-lookup"><span data-stu-id="c1c93-121">The user is available.</span></span>  <br/> |
|<span data-ttu-id="c1c93-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c1c93-122">0x00000001</span></span>  <br/> |<span data-ttu-id="c1c93-123">El usuario tiene un evento tentativa programado.</span><span class="sxs-lookup"><span data-stu-id="c1c93-123">The user has a tentative event scheduled.</span></span>  <br/> |
|<span data-ttu-id="c1c93-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c1c93-124">0x00000002</span></span>  <br/> |<span data-ttu-id="c1c93-125">El usuario está ocupado.</span><span class="sxs-lookup"><span data-stu-id="c1c93-125">The user is busy.</span></span>  <br/> |
|<span data-ttu-id="c1c93-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="c1c93-126">0x00000003</span></span>  <br/> |<span data-ttu-id="c1c93-127">El usuario no está en la oficina.</span><span class="sxs-lookup"><span data-stu-id="c1c93-127">The user is out of office.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c1c93-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1c93-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c1c93-129">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c1c93-129">Protocol specifications</span></span>

<span data-ttu-id="c1c93-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1c93-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1c93-131">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c1c93-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c1c93-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1c93-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1c93-133">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="c1c93-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c1c93-134">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c1c93-134">Header files</span></span>

<span data-ttu-id="c1c93-135">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c1c93-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="c1c93-136">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c1c93-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c1c93-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1c93-137">See also</span></span>



[<span data-ttu-id="c1c93-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c1c93-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c1c93-139">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="c1c93-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c1c93-140">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c1c93-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c1c93-141">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="c1c93-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

