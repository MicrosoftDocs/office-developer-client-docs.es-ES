---
title: Propiedad canónica PidLidTaskHistory
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskHistory
api_type:
- COM
ms.assetid: 104ef21c-b607-48b7-9b06-bc53b7d9b68a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6e53d91a80d7e3b3bb4bf02ff3446eb385293c6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818982"
---
# <a name="pidlidtaskhistory-canonical-property"></a><span data-ttu-id="e53e3-103">Propiedad canónica PidLidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="e53e3-103">PidLidTaskHistory Canonical Property</span></span>

  
  
<span data-ttu-id="e53e3-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e53e3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e53e3-105">Indica el tipo de cambio que se ha realizado la tarea por última vez.</span><span class="sxs-lookup"><span data-stu-id="e53e3-105">Indicates the type of change that was last made to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e53e3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e53e3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e53e3-107">dispidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="e53e3-107">dispidTaskHistory</span></span>  <br/> |
|<span data-ttu-id="e53e3-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e53e3-108">Property set:</span></span>  <br/> |<span data-ttu-id="e53e3-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="e53e3-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="e53e3-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="e53e3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e53e3-111">0x0000811A</span><span class="sxs-lookup"><span data-stu-id="e53e3-111">0x0000811A</span></span>  <br/> |
|<span data-ttu-id="e53e3-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e53e3-112">Data type:</span></span>  <br/> |<span data-ttu-id="e53e3-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e53e3-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e53e3-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e53e3-114">Area:</span></span>  <br/> |<span data-ttu-id="e53e3-115">Task</span><span class="sxs-lookup"><span data-stu-id="e53e3-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e53e3-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e53e3-116">Remarks</span></span>

<span data-ttu-id="e53e3-117">Cuando se establece el valor de esta propiedad, la propiedad **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) también debe establecerse en la hora actual.</span><span class="sxs-lookup"><span data-stu-id="e53e3-117">When the value of this property is set, the **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) property must also be set to the current time.</span></span> <span data-ttu-id="e53e3-118">En la siguiente tabla se muestra la **dispidTaskHistory** de valores de propiedad, que aparecen en el orden de prioridad de mayor a menor.</span><span class="sxs-lookup"><span data-stu-id="e53e3-118">The following table shows the **dispidTaskHistory** property values, listed in order of decreasing priority.</span></span> 
  
|<span data-ttu-id="e53e3-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e53e3-119">**Value**</span></span>|<span data-ttu-id="e53e3-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e53e3-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e53e3-121">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="e53e3-121">0x00000004</span></span>  <br/> |<span data-ttu-id="e53e3-122">La propiedad **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="e53e3-122">The **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property changed.</span></span>  <br/> |
|<span data-ttu-id="e53e3-123">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="e53e3-123">0x00000003</span></span>  <br/> |<span data-ttu-id="e53e3-124">Otra propiedad ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="e53e3-124">Another property was changed.</span></span>  <br/> |
|<span data-ttu-id="e53e3-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e53e3-125">0x00000001</span></span>  <br/> |<span data-ttu-id="e53e3-126">El encargado de la tarea había aceptada esta tarea.</span><span class="sxs-lookup"><span data-stu-id="e53e3-126">The task assignee accepted this task.</span></span>  <br/> |
|<span data-ttu-id="e53e3-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e53e3-127">0x00000002</span></span>  <br/> |<span data-ttu-id="e53e3-128">El encargado de la tarea rechaza esta tarea.</span><span class="sxs-lookup"><span data-stu-id="e53e3-128">The task assignee rejected this task.</span></span>  <br/> |
|<span data-ttu-id="e53e3-129">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="e53e3-129">0x00000005</span></span>  <br/> |<span data-ttu-id="e53e3-130">La tarea se ha asignado a un encargado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="e53e3-130">The task was assigned to a task assignee.</span></span>  <br/> |
|<span data-ttu-id="e53e3-131">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e53e3-131">0x00000000</span></span>  <br/> |<span data-ttu-id="e53e3-132">No se realizaron cambios.</span><span class="sxs-lookup"><span data-stu-id="e53e3-132">No changes were made.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e53e3-133">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e53e3-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e53e3-134">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e53e3-134">Protocol specifications</span></span>

<span data-ttu-id="e53e3-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e53e3-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e53e3-136">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e53e3-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e53e3-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e53e3-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e53e3-138">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="e53e3-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e53e3-139">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e53e3-139">Header files</span></span>

<span data-ttu-id="e53e3-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e53e3-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="e53e3-141">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e53e3-141">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e53e3-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="e53e3-142">See also</span></span>



[<span data-ttu-id="e53e3-143">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e53e3-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e53e3-144">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e53e3-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e53e3-145">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e53e3-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e53e3-146">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e53e3-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

