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
ms.openlocfilehash: d0ae319a6b5fa4c901ec7d318c7ebdd216a2adeb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357942"
---
# <a name="pidlidtaskmode-canonical-property"></a><span data-ttu-id="5964e-103">Propiedad canónica PidLidTaskMode</span><span class="sxs-lookup"><span data-stu-id="5964e-103">PidLidTaskMode Canonical Property</span></span>

  
  
<span data-ttu-id="5964e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5964e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5964e-105">Especifica el estado de asignación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="5964e-105">Specifies the assignment status of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5964e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5964e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5964e-107">dispidTaskMode</span><span class="sxs-lookup"><span data-stu-id="5964e-107">dispidTaskMode</span></span>  <br/> |
|<span data-ttu-id="5964e-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="5964e-108">Property set:</span></span>  <br/> |<span data-ttu-id="5964e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5964e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5964e-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5964e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5964e-111">0x00008518</span><span class="sxs-lookup"><span data-stu-id="5964e-111">0x00008518</span></span>  <br/> |
|<span data-ttu-id="5964e-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5964e-112">Data type:</span></span>  <br/> |<span data-ttu-id="5964e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5964e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5964e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5964e-114">Area:</span></span>  <br/> |<span data-ttu-id="5964e-115">Task</span><span class="sxs-lookup"><span data-stu-id="5964e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5964e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5964e-116">Remarks</span></span>

<span data-ttu-id="5964e-117">El valor debe ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="5964e-117">The value must be one of the following.</span></span>
  
|<span data-ttu-id="5964e-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5964e-118">**Value**</span></span>|<span data-ttu-id="5964e-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5964e-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5964e-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5964e-120">0x00000000</span></span>  <br/> |<span data-ttu-id="5964e-121">La tarea no está asignada.</span><span class="sxs-lookup"><span data-stu-id="5964e-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="5964e-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5964e-122">0x00000001</span></span>  <br/> |<span data-ttu-id="5964e-123">La tarea está incrustada en una solicitud de tarea.</span><span class="sxs-lookup"><span data-stu-id="5964e-123">The task is embedded in a task request.</span></span>  <br/> |
|<span data-ttu-id="5964e-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5964e-124">0x00000002</span></span>  <br/> |<span data-ttu-id="5964e-125">La tarea fue aceptada por el usuario al que se asigna la tarea.</span><span class="sxs-lookup"><span data-stu-id="5964e-125">The task was accepted by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="5964e-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="5964e-126">0x00000003</span></span>  <br/> |<span data-ttu-id="5964e-127">El usuario al que se asigna la tarea rechazó la tarea.</span><span class="sxs-lookup"><span data-stu-id="5964e-127">The task was rejected by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="5964e-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5964e-128">0x00000004</span></span>  <br/> |<span data-ttu-id="5964e-129">La tarea está incrustada en una actualización de tarea.</span><span class="sxs-lookup"><span data-stu-id="5964e-129">The task is embedded in a task update.</span></span>  <br/> |
|<span data-ttu-id="5964e-130">0x00000005</span><span class="sxs-lookup"><span data-stu-id="5964e-130">0x00000005</span></span>  <br/> |<span data-ttu-id="5964e-131">La tarea se asignó al asignador de tareas.</span><span class="sxs-lookup"><span data-stu-id="5964e-131">The task was assigned to the task assigner.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5964e-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5964e-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5964e-133">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="5964e-133">Protocol specifications</span></span>

<span data-ttu-id="5964e-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5964e-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5964e-135">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="5964e-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5964e-136">[[MS-OJOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5964e-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5964e-137">Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="5964e-137">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5964e-138">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5964e-138">Header files</span></span>

<span data-ttu-id="5964e-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5964e-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="5964e-140">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5964e-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5964e-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5964e-141">See also</span></span>



[<span data-ttu-id="5964e-142">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5964e-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5964e-143">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="5964e-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5964e-144">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5964e-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5964e-145">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="5964e-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

