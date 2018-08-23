---
title: Propiedad canónica PidLidTaskAcceptanceState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAcceptanceState
api_type:
- COM
ms.assetid: 7012f524-bc66-48ea-85b5-163e05029d35
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b4124a319f378ff2c60de7a1fddaa549aeb08a05
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583333"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a><span data-ttu-id="88147-103">Propiedad canónica PidLidTaskAcceptanceState</span><span class="sxs-lookup"><span data-stu-id="88147-103">PidLidTaskAcceptanceState Canonical Property</span></span>

  
  
<span data-ttu-id="88147-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88147-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88147-105">Indica el estado de aceptación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="88147-105">Indicates the acceptance state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="88147-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="88147-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="88147-107">dispidTaskDelegValue</span><span class="sxs-lookup"><span data-stu-id="88147-107">dispidTaskDelegValue</span></span>  <br/> |
|<span data-ttu-id="88147-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="88147-108">Property set:</span></span>  <br/> |<span data-ttu-id="88147-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="88147-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="88147-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="88147-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="88147-111">0x0000812A</span><span class="sxs-lookup"><span data-stu-id="88147-111">0x0000812A</span></span>  <br/> |
|<span data-ttu-id="88147-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="88147-112">Data type:</span></span>  <br/> |<span data-ttu-id="88147-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="88147-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="88147-114">Área:</span><span class="sxs-lookup"><span data-stu-id="88147-114">Area:</span></span>  <br/> |<span data-ttu-id="88147-115">Task</span><span class="sxs-lookup"><span data-stu-id="88147-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88147-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="88147-116">Remarks</span></span>

<span data-ttu-id="88147-117">La siguiente tabla muestran los valores posibles para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="88147-117">The following table shows the possible values for this property.</span></span>
  
|<span data-ttu-id="88147-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="88147-118">**Value**</span></span>|<span data-ttu-id="88147-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="88147-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="88147-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88147-120">0x00000000</span></span>  <br/> |<span data-ttu-id="88147-121">No se asigna la tarea.</span><span class="sxs-lookup"><span data-stu-id="88147-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="88147-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="88147-122">0x00000001</span></span>  <br/> |<span data-ttu-id="88147-123">Estado de aceptación de la tarea es desconocido.</span><span class="sxs-lookup"><span data-stu-id="88147-123">The task's acceptance status is unknown.</span></span>  <br/> |
|<span data-ttu-id="88147-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="88147-124">0x00000002</span></span>  <br/> |<span data-ttu-id="88147-125">El encargado de la tarea aceptó la tarea.</span><span class="sxs-lookup"><span data-stu-id="88147-125">The task assignee accepted the task.</span></span> <span data-ttu-id="88147-126">Este valor se establece cuando el cliente procesa una aceptación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="88147-126">This value is set when the client processes a task acceptance.</span></span>  <br/> |
|<span data-ttu-id="88147-127">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="88147-127">0x00000003</span></span>  <br/> |<span data-ttu-id="88147-128">El encargado de la tarea, rechaza la tarea.</span><span class="sxs-lookup"><span data-stu-id="88147-128">The task assignee rejected the task.</span></span> <span data-ttu-id="88147-129">Este valor se establece cuando el cliente procesa un rechazo de tarea.</span><span class="sxs-lookup"><span data-stu-id="88147-129">This value is set when the client processes a task rejection.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="88147-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="88147-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="88147-131">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="88147-131">Protocol specifications</span></span>

<span data-ttu-id="88147-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88147-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88147-133">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="88147-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="88147-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88147-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88147-135">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="88147-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="88147-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="88147-136">Header files</span></span>

<span data-ttu-id="88147-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="88147-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="88147-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="88147-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="88147-139">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="88147-139">See also</span></span>



[<span data-ttu-id="88147-140">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="88147-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="88147-141">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="88147-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="88147-142">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="88147-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="88147-143">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="88147-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

