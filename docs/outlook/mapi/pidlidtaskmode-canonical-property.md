---
title: Propiedad canónica PidLidTaskMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMode
api_type:
- COM
ms.assetid: 185db683-301a-4d91-a583-6959853fa1ad
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bc8e4dfe934d516c07d5532ba6a95e51a3cbf962
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578083"
---
# <a name="pidlidtaskmode-canonical-property"></a><span data-ttu-id="5e0ba-103">Propiedad canónica PidLidTaskMode</span><span class="sxs-lookup"><span data-stu-id="5e0ba-103">PidLidTaskMode Canonical Property</span></span>

  
  
<span data-ttu-id="5e0ba-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e0ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e0ba-105">Especifica el estado de asignación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="5e0ba-105">Specifies the assignment status of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e0ba-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5e0ba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e0ba-107">dispidTaskMode</span><span class="sxs-lookup"><span data-stu-id="5e0ba-107">dispidTaskMode</span></span>  <br/> |
|<span data-ttu-id="5e0ba-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="5e0ba-108">Property set:</span></span>  <br/> |<span data-ttu-id="5e0ba-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5e0ba-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5e0ba-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="5e0ba-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5e0ba-111">0x00008518</span><span class="sxs-lookup"><span data-stu-id="5e0ba-111">0x00008518</span></span>  <br/> |
|<span data-ttu-id="5e0ba-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5e0ba-112">Data type:</span></span>  <br/> |<span data-ttu-id="5e0ba-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5e0ba-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5e0ba-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5e0ba-114">Area:</span></span>  <br/> |<span data-ttu-id="5e0ba-115">Task</span><span class="sxs-lookup"><span data-stu-id="5e0ba-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e0ba-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5e0ba-116">Remarks</span></span>

<span data-ttu-id="5e0ba-117">El valor debe ser una de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="5e0ba-117">The value must be one of the following.</span></span>
  
|<span data-ttu-id="5e0ba-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5e0ba-118">**Value**</span></span>|<span data-ttu-id="5e0ba-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5e0ba-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5e0ba-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5e0ba-120">0x00000000</span></span>  <br/> |<span data-ttu-id="5e0ba-121">No se asigna la tarea.</span><span class="sxs-lookup"><span data-stu-id="5e0ba-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="5e0ba-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5e0ba-122">0x00000001</span></span>  <br/> |<span data-ttu-id="5e0ba-123">La tarea está incrustada en una solicitud de tarea.</span><span class="sxs-lookup"><span data-stu-id="5e0ba-123">The task is embedded in a task request.</span></span>  <br/> |
|<span data-ttu-id="5e0ba-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5e0ba-124">0x00000002</span></span>  <br/> |<span data-ttu-id="5e0ba-125">La tarea se ha aceptado por el encargado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="5e0ba-125">The task was accepted by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="5e0ba-126">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="5e0ba-126">0x00000003</span></span>  <br/> |<span data-ttu-id="5e0ba-127">La tarea fue rechazada por el encargado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="5e0ba-127">The task was rejected by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="5e0ba-128">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="5e0ba-128">0x00000004</span></span>  <br/> |<span data-ttu-id="5e0ba-129">La tarea está incrustada en una actualización de la tarea.</span><span class="sxs-lookup"><span data-stu-id="5e0ba-129">The task is embedded in a task update.</span></span>  <br/> |
|<span data-ttu-id="5e0ba-130">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="5e0ba-130">0x00000005</span></span>  <br/> |<span data-ttu-id="5e0ba-131">Se asignó la tarea para el asignador de tareas.</span><span class="sxs-lookup"><span data-stu-id="5e0ba-131">The task was assigned to the task assigner.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5e0ba-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e0ba-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5e0ba-133">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5e0ba-133">Protocol specifications</span></span>

<span data-ttu-id="5e0ba-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e0ba-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e0ba-135">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5e0ba-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5e0ba-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e0ba-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e0ba-137">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="5e0ba-137">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5e0ba-138">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5e0ba-138">Header files</span></span>

<span data-ttu-id="5e0ba-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e0ba-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e0ba-140">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5e0ba-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e0ba-141">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5e0ba-141">See also</span></span>



[<span data-ttu-id="5e0ba-142">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5e0ba-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e0ba-143">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5e0ba-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e0ba-144">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5e0ba-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e0ba-145">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5e0ba-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

