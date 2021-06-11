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
ms.openlocfilehash: 39f2e6aeb4026f0b33be08b3bd8123283e5df3e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303013"
---
# <a name="pidlidtaskhistory-canonical-property"></a><span data-ttu-id="2443b-103">Propiedad canónica PidLidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="2443b-103">PidLidTaskHistory Canonical Property</span></span>

  
  
<span data-ttu-id="2443b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2443b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2443b-105">Indica el tipo de cambio que se realizó por última vez en la tarea.</span><span class="sxs-lookup"><span data-stu-id="2443b-105">Indicates the type of change that was last made to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2443b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2443b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2443b-107">dispidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="2443b-107">dispidTaskHistory</span></span>  <br/> |
|<span data-ttu-id="2443b-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="2443b-108">Property set:</span></span>  <br/> |<span data-ttu-id="2443b-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="2443b-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="2443b-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="2443b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2443b-111">0x0000811A</span><span class="sxs-lookup"><span data-stu-id="2443b-111">0x0000811A</span></span>  <br/> |
|<span data-ttu-id="2443b-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2443b-112">Data type:</span></span>  <br/> |<span data-ttu-id="2443b-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2443b-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2443b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="2443b-114">Area:</span></span>  <br/> |<span data-ttu-id="2443b-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="2443b-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2443b-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2443b-116">Remarks</span></span>

<span data-ttu-id="2443b-117">Cuando se establece el valor de esta propiedad, la propiedad **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) también debe establecerse en la hora actual.</span><span class="sxs-lookup"><span data-stu-id="2443b-117">When the value of this property is set, the **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) property must also be set to the current time.</span></span> <span data-ttu-id="2443b-118">En la tabla siguiente se muestran los valores de la propiedad **dispidTaskHistory,** enumerados en orden de disminución de prioridad.</span><span class="sxs-lookup"><span data-stu-id="2443b-118">The following table shows the **dispidTaskHistory** property values, listed in order of decreasing priority.</span></span> 
  
|<span data-ttu-id="2443b-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2443b-119">**Value**</span></span>|<span data-ttu-id="2443b-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2443b-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2443b-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2443b-121">0x00000004</span></span>  <br/> |<span data-ttu-id="2443b-122">La **propiedad dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="2443b-122">The **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property changed.</span></span>  <br/> |
|<span data-ttu-id="2443b-123">0x00000003</span><span class="sxs-lookup"><span data-stu-id="2443b-123">0x00000003</span></span>  <br/> |<span data-ttu-id="2443b-124">Se cambió otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="2443b-124">Another property was changed.</span></span>  <br/> |
|<span data-ttu-id="2443b-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2443b-125">0x00000001</span></span>  <br/> |<span data-ttu-id="2443b-126">El destinatario de la tarea aceptó esta tarea.</span><span class="sxs-lookup"><span data-stu-id="2443b-126">The task assignee accepted this task.</span></span>  <br/> |
|<span data-ttu-id="2443b-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2443b-127">0x00000002</span></span>  <br/> |<span data-ttu-id="2443b-128">El destinatario de la tarea rechazó esta tarea.</span><span class="sxs-lookup"><span data-stu-id="2443b-128">The task assignee rejected this task.</span></span>  <br/> |
|<span data-ttu-id="2443b-129">0x00000005</span><span class="sxs-lookup"><span data-stu-id="2443b-129">0x00000005</span></span>  <br/> |<span data-ttu-id="2443b-130">La tarea se asignó a un usuario asignado.</span><span class="sxs-lookup"><span data-stu-id="2443b-130">The task was assigned to a task assignee.</span></span>  <br/> |
|<span data-ttu-id="2443b-131">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2443b-131">0x00000000</span></span>  <br/> |<span data-ttu-id="2443b-132">No se realizaron cambios.</span><span class="sxs-lookup"><span data-stu-id="2443b-132">No changes were made.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2443b-133">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2443b-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2443b-134">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="2443b-134">Protocol specifications</span></span>

<span data-ttu-id="2443b-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2443b-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2443b-136">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="2443b-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2443b-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2443b-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2443b-138">Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="2443b-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2443b-139">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2443b-139">Header files</span></span>

<span data-ttu-id="2443b-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2443b-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="2443b-141">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2443b-141">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2443b-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="2443b-142">See also</span></span>



[<span data-ttu-id="2443b-143">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2443b-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2443b-144">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2443b-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2443b-145">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2443b-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2443b-146">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2443b-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

