---
title: Propiedad canónica PidLidTaskState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskState
api_type:
- COM
ms.assetid: 06d1f8a3-53e1-4c9a-9703-75de7a11a772
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 149f238ea53e0669f4d95c8e6c2b17a2b5a1c209
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316538"
---
# <a name="pidlidtaskstate-canonical-property"></a><span data-ttu-id="97b56-103">Propiedad canónica PidLidTaskState</span><span class="sxs-lookup"><span data-stu-id="97b56-103">PidLidTaskState Canonical Property</span></span>

  
  
<span data-ttu-id="97b56-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97b56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97b56-105">Indica el estado de asignación actual de la tarea.</span><span class="sxs-lookup"><span data-stu-id="97b56-105">Indicates the current assignment state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97b56-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="97b56-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="97b56-107">dispidTaskState</span><span class="sxs-lookup"><span data-stu-id="97b56-107">dispidTaskState</span></span>  <br/> |
|<span data-ttu-id="97b56-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="97b56-108">Property set:</span></span>  <br/> |<span data-ttu-id="97b56-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="97b56-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="97b56-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="97b56-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="97b56-111">0x00008113</span><span class="sxs-lookup"><span data-stu-id="97b56-111">0x00008113</span></span>  <br/> |
|<span data-ttu-id="97b56-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="97b56-112">Data type:</span></span>  <br/> |<span data-ttu-id="97b56-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="97b56-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="97b56-114">Área:</span><span class="sxs-lookup"><span data-stu-id="97b56-114">Area:</span></span>  <br/> |<span data-ttu-id="97b56-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="97b56-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97b56-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="97b56-116">Remarks</span></span>

<span data-ttu-id="97b56-117">El valor de esta propiedad debe ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="97b56-117">The value of this property must be one of the following.</span></span>
  
|<span data-ttu-id="97b56-118">**Value**</span><span class="sxs-lookup"><span data-stu-id="97b56-118">**Value**</span></span>|<span data-ttu-id="97b56-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="97b56-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="97b56-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97b56-120">0x00000000</span></span>  <br/> |<span data-ttu-id="97b56-121">Esta tarea se creó para coincidir con una tarea que se incrustó en un rechazo de tarea pero que no se pudo encontrar localmente.</span><span class="sxs-lookup"><span data-stu-id="97b56-121">This task was created to correspond to a task that was embedded in a task rejection but could not be found locally.</span></span>  <br/> |
|<span data-ttu-id="97b56-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="97b56-122">0x00000001</span></span>  <br/> |<span data-ttu-id="97b56-123">La tarea no está asignada.</span><span class="sxs-lookup"><span data-stu-id="97b56-123">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="97b56-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="97b56-124">0x00000002</span></span>  <br/> |<span data-ttu-id="97b56-125">La tarea es la copia del destinatario de la tarea de una tarea asignada.</span><span class="sxs-lookup"><span data-stu-id="97b56-125">The task is the task assignee's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="97b56-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="97b56-126">0x00000003</span></span>  <br/> |<span data-ttu-id="97b56-127">La tarea es la copia del encargado de la tarea de una tarea asignada.</span><span class="sxs-lookup"><span data-stu-id="97b56-127">The task is the task assigner's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="97b56-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="97b56-128">0x00000004</span></span>  <br/> |<span data-ttu-id="97b56-129">La tarea es la copia del encargado de la tarea de una tarea rechazada.</span><span class="sxs-lookup"><span data-stu-id="97b56-129">The task is the task assigner's copy of a rejected task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="97b56-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="97b56-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="97b56-131">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="97b56-131">Protocol specifications</span></span>

<span data-ttu-id="97b56-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97b56-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97b56-133">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="97b56-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="97b56-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97b56-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97b56-135">Define varios objetos que modelan el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="97b56-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="97b56-136">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97b56-136">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97b56-137">Especifica las propiedades y operaciones para crear y ubicar las carpetas especiales en un buzón.</span><span class="sxs-lookup"><span data-stu-id="97b56-137">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="97b56-138">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97b56-138">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97b56-139">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="97b56-139">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="97b56-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97b56-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97b56-141">Controla el orden y el flujo de transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="97b56-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="97b56-142">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="97b56-142">Header files</span></span>

<span data-ttu-id="97b56-143">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="97b56-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="97b56-144">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="97b56-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97b56-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="97b56-145">See also</span></span>



[<span data-ttu-id="97b56-146">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="97b56-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="97b56-147">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="97b56-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="97b56-148">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="97b56-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="97b56-149">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="97b56-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

