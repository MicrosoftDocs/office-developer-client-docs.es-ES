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
ms.openlocfilehash: 926f0425a4a59cad4280917573c974375c94f50b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818587"
---
# <a name="pidlidbusystatus-canonical-property"></a><span data-ttu-id="23eb6-103">Propiedad canónica PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="23eb6-103">PidLidBusyStatus Canonical Property</span></span>

  
  
<span data-ttu-id="23eb6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23eb6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="23eb6-105">Representa la disponibilidad del usuario para una cita.</span><span class="sxs-lookup"><span data-stu-id="23eb6-105">Represents the user's availability for an appointment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23eb6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="23eb6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23eb6-107">dispidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="23eb6-107">dispidBusyStatus</span></span>  <br/> |
|<span data-ttu-id="23eb6-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="23eb6-108">Property set:</span></span>  <br/> |<span data-ttu-id="23eb6-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="23eb6-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="23eb6-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="23eb6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="23eb6-111">0x00008205</span><span class="sxs-lookup"><span data-stu-id="23eb6-111">0x00008205</span></span>  <br/> |
|<span data-ttu-id="23eb6-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="23eb6-112">Data type:</span></span>  <br/> |<span data-ttu-id="23eb6-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="23eb6-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="23eb6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="23eb6-114">Area:</span></span>  <br/> |<span data-ttu-id="23eb6-115">Calendario</span><span class="sxs-lookup"><span data-stu-id="23eb6-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23eb6-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="23eb6-116">Remarks</span></span>

<span data-ttu-id="23eb6-117">Esta propiedad especifica la disponibilidad de un usuario para el evento descrito por el objeto y debe ser uno de los valores especificados por debajo.</span><span class="sxs-lookup"><span data-stu-id="23eb6-117">This property specifies the availability of a user for the event described by the object and must be one of the values specified below.</span></span>
  
|<span data-ttu-id="23eb6-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="23eb6-118">**Value**</span></span>|<span data-ttu-id="23eb6-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="23eb6-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="23eb6-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23eb6-120">0x00000000</span></span>  <br/> |<span data-ttu-id="23eb6-121">El usuario está disponible.</span><span class="sxs-lookup"><span data-stu-id="23eb6-121">The user is available.</span></span>  <br/> |
|<span data-ttu-id="23eb6-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="23eb6-122">0x00000001</span></span>  <br/> |<span data-ttu-id="23eb6-123">El usuario tiene un evento provisional programado.</span><span class="sxs-lookup"><span data-stu-id="23eb6-123">The user has a tentative event scheduled.</span></span>  <br/> |
|<span data-ttu-id="23eb6-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="23eb6-124">0x00000002</span></span>  <br/> |<span data-ttu-id="23eb6-125">El usuario está ocupado.</span><span class="sxs-lookup"><span data-stu-id="23eb6-125">The user is busy.</span></span>  <br/> |
|<span data-ttu-id="23eb6-126">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="23eb6-126">0x00000003</span></span>  <br/> |<span data-ttu-id="23eb6-127">El usuario no está en la oficina.</span><span class="sxs-lookup"><span data-stu-id="23eb6-127">The user is out of office.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="23eb6-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="23eb6-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="23eb6-129">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="23eb6-129">Protocol specifications</span></span>

<span data-ttu-id="23eb6-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23eb6-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23eb6-131">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="23eb6-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="23eb6-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23eb6-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23eb6-133">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="23eb6-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="23eb6-134">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="23eb6-134">Header files</span></span>

<span data-ttu-id="23eb6-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="23eb6-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="23eb6-136">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="23eb6-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23eb6-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="23eb6-137">See also</span></span>



[<span data-ttu-id="23eb6-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="23eb6-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23eb6-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="23eb6-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23eb6-140">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="23eb6-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23eb6-141">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="23eb6-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

