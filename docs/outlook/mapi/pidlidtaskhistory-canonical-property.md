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
# <a name="pidlidtaskhistory-canonical-property"></a><span data-ttu-id="80b3e-103">Propiedad canónica PidLidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="80b3e-103">PidLidTaskHistory Canonical Property</span></span>

  
  
<span data-ttu-id="80b3e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80b3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80b3e-105">Indica el tipo de cambio que se realizó por última vez en la tarea.</span><span class="sxs-lookup"><span data-stu-id="80b3e-105">Indicates the type of change that was last made to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80b3e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="80b3e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80b3e-107">dispidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="80b3e-107">dispidTaskHistory</span></span>  <br/> |
|<span data-ttu-id="80b3e-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="80b3e-108">Property set:</span></span>  <br/> |<span data-ttu-id="80b3e-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="80b3e-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="80b3e-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="80b3e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="80b3e-111">0x0000811A</span><span class="sxs-lookup"><span data-stu-id="80b3e-111">0x0000811A</span></span>  <br/> |
|<span data-ttu-id="80b3e-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="80b3e-112">Data type:</span></span>  <br/> |<span data-ttu-id="80b3e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="80b3e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="80b3e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="80b3e-114">Area:</span></span>  <br/> |<span data-ttu-id="80b3e-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="80b3e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80b3e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="80b3e-116">Remarks</span></span>

<span data-ttu-id="80b3e-117">Cuando se establece el valor de esta propiedad, la propiedad **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) también debe establecerse en la hora actual.</span><span class="sxs-lookup"><span data-stu-id="80b3e-117">When the value of this property is set, the **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) property must also be set to the current time.</span></span> <span data-ttu-id="80b3e-118">En la siguiente tabla se muestran los valores de propiedad de **dispidTaskHistory** , enumerados por orden de prioridad descendente.</span><span class="sxs-lookup"><span data-stu-id="80b3e-118">The following table shows the **dispidTaskHistory** property values, listed in order of decreasing priority.</span></span> 
  
|<span data-ttu-id="80b3e-119">**Value**</span><span class="sxs-lookup"><span data-stu-id="80b3e-119">**Value**</span></span>|<span data-ttu-id="80b3e-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="80b3e-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="80b3e-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="80b3e-121">0x00000004</span></span>  <br/> |<span data-ttu-id="80b3e-122">La propiedad **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="80b3e-122">The **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property changed.</span></span>  <br/> |
|<span data-ttu-id="80b3e-123">0x00000003</span><span class="sxs-lookup"><span data-stu-id="80b3e-123">0x00000003</span></span>  <br/> |<span data-ttu-id="80b3e-124">Se cambió otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="80b3e-124">Another property was changed.</span></span>  <br/> |
|<span data-ttu-id="80b3e-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="80b3e-125">0x00000001</span></span>  <br/> |<span data-ttu-id="80b3e-126">El usuario al que se le asigna la tarea aceptó esta tarea.</span><span class="sxs-lookup"><span data-stu-id="80b3e-126">The task assignee accepted this task.</span></span>  <br/> |
|<span data-ttu-id="80b3e-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="80b3e-127">0x00000002</span></span>  <br/> |<span data-ttu-id="80b3e-128">El usuario al que se asigna una tarea rechazó esta tarea.</span><span class="sxs-lookup"><span data-stu-id="80b3e-128">The task assignee rejected this task.</span></span>  <br/> |
|<span data-ttu-id="80b3e-129">0x00000005</span><span class="sxs-lookup"><span data-stu-id="80b3e-129">0x00000005</span></span>  <br/> |<span data-ttu-id="80b3e-130">La tarea se asignó a un usuario al que se le ha asignado una tarea.</span><span class="sxs-lookup"><span data-stu-id="80b3e-130">The task was assigned to a task assignee.</span></span>  <br/> |
|<span data-ttu-id="80b3e-131">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80b3e-131">0x00000000</span></span>  <br/> |<span data-ttu-id="80b3e-132">No se han realizado cambios.</span><span class="sxs-lookup"><span data-stu-id="80b3e-132">No changes were made.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="80b3e-133">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="80b3e-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="80b3e-134">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="80b3e-134">Protocol specifications</span></span>

<span data-ttu-id="80b3e-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80b3e-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80b3e-136">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="80b3e-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="80b3e-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80b3e-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80b3e-138">Define varios objetos que modelan el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="80b3e-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="80b3e-139">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="80b3e-139">Header files</span></span>

<span data-ttu-id="80b3e-140">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="80b3e-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="80b3e-141">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="80b3e-141">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80b3e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="80b3e-142">See also</span></span>



[<span data-ttu-id="80b3e-143">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="80b3e-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80b3e-144">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="80b3e-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80b3e-145">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="80b3e-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80b3e-146">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="80b3e-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

