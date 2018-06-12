---
title: Propiedad canónico PidLidTaskState
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: b4bab1948bc563b92dafa16922da3b9760cf1a1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818995"
---
# <a name="pidlidtaskstate-canonical-property"></a><span data-ttu-id="d21ed-103">Propiedad canónico PidLidTaskState</span><span class="sxs-lookup"><span data-stu-id="d21ed-103">PidLidTaskState Canonical Property</span></span>

  
  
<span data-ttu-id="d21ed-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d21ed-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d21ed-105">Indica el estado actual de la asignación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="d21ed-105">Indicates the current assignment state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d21ed-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d21ed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d21ed-107">dispidTaskState</span><span class="sxs-lookup"><span data-stu-id="d21ed-107">dispidTaskState</span></span>  <br/> |
|<span data-ttu-id="d21ed-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="d21ed-108">Property set:</span></span>  <br/> |<span data-ttu-id="d21ed-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="d21ed-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="d21ed-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="d21ed-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d21ed-111">0x00008113</span><span class="sxs-lookup"><span data-stu-id="d21ed-111">0x00008113</span></span>  <br/> |
|<span data-ttu-id="d21ed-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d21ed-112">Data type:</span></span>  <br/> |<span data-ttu-id="d21ed-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d21ed-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d21ed-114">Área:</span><span class="sxs-lookup"><span data-stu-id="d21ed-114">Area:</span></span>  <br/> |<span data-ttu-id="d21ed-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="d21ed-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d21ed-116">Notas</span><span class="sxs-lookup"><span data-stu-id="d21ed-116">Remarks</span></span>

<span data-ttu-id="d21ed-117">El valor de esta propiedad debe ser una de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="d21ed-117">The value of this property must be one of the following.</span></span>
  
|<span data-ttu-id="d21ed-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d21ed-118">**Value**</span></span>|<span data-ttu-id="d21ed-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d21ed-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d21ed-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d21ed-120">0x00000000</span></span>  <br/> |<span data-ttu-id="d21ed-121">Esta tarea se creó para corresponden a una tarea que se ha incrustado en un rechazo de la tarea, pero no se pudo encontrar localmente.</span><span class="sxs-lookup"><span data-stu-id="d21ed-121">This task was created to correspond to a task that was embedded in a task rejection but could not be found locally.</span></span>  <br/> |
|<span data-ttu-id="d21ed-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d21ed-122">0x00000001</span></span>  <br/> |<span data-ttu-id="d21ed-123">No se asigna la tarea.</span><span class="sxs-lookup"><span data-stu-id="d21ed-123">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="d21ed-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d21ed-124">0x00000002</span></span>  <br/> |<span data-ttu-id="d21ed-125">La tarea es copia del encargado de la tarea de una tarea asignada.</span><span class="sxs-lookup"><span data-stu-id="d21ed-125">The task is the task assignee's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="d21ed-126">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="d21ed-126">0x00000003</span></span>  <br/> |<span data-ttu-id="d21ed-127">La tarea es copia del asignador de tarea de una tarea asignada.</span><span class="sxs-lookup"><span data-stu-id="d21ed-127">The task is the task assigner's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="d21ed-128">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="d21ed-128">0x00000004</span></span>  <br/> |<span data-ttu-id="d21ed-129">La tarea es copia del asignador de tarea de una tarea rechazada.</span><span class="sxs-lookup"><span data-stu-id="d21ed-129">The task is the task assigner's copy of a rejected task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d21ed-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d21ed-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d21ed-131">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d21ed-131">Protocol specifications</span></span>

<span data-ttu-id="d21ed-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d21ed-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d21ed-133">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d21ed-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d21ed-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d21ed-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d21ed-135">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="d21ed-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="d21ed-136">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d21ed-136">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d21ed-137">Especifica las propiedades y operaciones para la creación y la ubicación de las carpetas especiales en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d21ed-137">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="d21ed-138">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d21ed-138">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d21ed-139">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="d21ed-139">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="d21ed-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d21ed-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d21ed-141">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="d21ed-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d21ed-142">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d21ed-142">Header files</span></span>

<span data-ttu-id="d21ed-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d21ed-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="d21ed-144">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d21ed-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d21ed-145">Ver también</span><span class="sxs-lookup"><span data-stu-id="d21ed-145">See also</span></span>



[<span data-ttu-id="d21ed-146">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d21ed-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d21ed-147">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d21ed-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d21ed-148">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="d21ed-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d21ed-149">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d21ed-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

