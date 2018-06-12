---
title: Propiedad canónico PidLidBusyStatus
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 926f0425a4a59cad4280917573c974375c94f50b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818587"
---
# <a name="pidlidbusystatus-canonical-property"></a><span data-ttu-id="59877-103">Propiedad canónico PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="59877-103">PidLidBusyStatus Canonical Property</span></span>

  
  
<span data-ttu-id="59877-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="59877-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="59877-105">Representa la disponibilidad del usuario para una cita.</span><span class="sxs-lookup"><span data-stu-id="59877-105">Represents the user's availability for an appointment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="59877-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="59877-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="59877-107">dispidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="59877-107">dispidBusyStatus</span></span>  <br/> |
|<span data-ttu-id="59877-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="59877-108">Property set:</span></span>  <br/> |<span data-ttu-id="59877-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="59877-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="59877-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="59877-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="59877-111">0x00008205</span><span class="sxs-lookup"><span data-stu-id="59877-111">0x00008205</span></span>  <br/> |
|<span data-ttu-id="59877-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="59877-112">Data type:</span></span>  <br/> |<span data-ttu-id="59877-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="59877-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="59877-114">Área:</span><span class="sxs-lookup"><span data-stu-id="59877-114">Area:</span></span>  <br/> |<span data-ttu-id="59877-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="59877-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59877-116">Notas</span><span class="sxs-lookup"><span data-stu-id="59877-116">Remarks</span></span>

<span data-ttu-id="59877-117">Esta propiedad especifica la disponibilidad de un usuario para el evento descrito por el objeto y debe ser uno de los valores especificados por debajo.</span><span class="sxs-lookup"><span data-stu-id="59877-117">This property specifies the availability of a user for the event described by the object and must be one of the values specified below.</span></span>
  
|<span data-ttu-id="59877-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="59877-118">**Value**</span></span>|<span data-ttu-id="59877-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="59877-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="59877-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59877-120">0x00000000</span></span>  <br/> |<span data-ttu-id="59877-121">El usuario está disponible.</span><span class="sxs-lookup"><span data-stu-id="59877-121">The user is available.</span></span>  <br/> |
|<span data-ttu-id="59877-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="59877-122">0x00000001</span></span>  <br/> |<span data-ttu-id="59877-123">El usuario tiene un evento provisional programado.</span><span class="sxs-lookup"><span data-stu-id="59877-123">The user has a tentative event scheduled.</span></span>  <br/> |
|<span data-ttu-id="59877-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="59877-124">0x00000002</span></span>  <br/> |<span data-ttu-id="59877-125">El usuario está ocupado.</span><span class="sxs-lookup"><span data-stu-id="59877-125">The user is busy.</span></span>  <br/> |
|<span data-ttu-id="59877-126">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="59877-126">0x00000003</span></span>  <br/> |<span data-ttu-id="59877-127">El usuario no está en la oficina.</span><span class="sxs-lookup"><span data-stu-id="59877-127">The user is out of office.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="59877-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="59877-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="59877-129">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="59877-129">Protocol specifications</span></span>

<span data-ttu-id="59877-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59877-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59877-131">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="59877-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="59877-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59877-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59877-133">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="59877-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="59877-134">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="59877-134">Header files</span></span>

<span data-ttu-id="59877-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="59877-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="59877-136">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="59877-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59877-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="59877-137">See also</span></span>



[<span data-ttu-id="59877-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="59877-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="59877-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="59877-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="59877-140">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="59877-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="59877-141">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="59877-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

