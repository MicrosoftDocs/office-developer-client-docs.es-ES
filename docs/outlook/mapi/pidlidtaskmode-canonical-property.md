---
title: Propiedad canónico PidLidTaskMode
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: f8eef7863cec565403d41dae26687b75f078e0d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818987"
---
# <a name="pidlidtaskmode-canonical-property"></a><span data-ttu-id="a420e-103">Propiedad canónico PidLidTaskMode</span><span class="sxs-lookup"><span data-stu-id="a420e-103">PidLidTaskMode Canonical Property</span></span>

  
  
<span data-ttu-id="a420e-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a420e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a420e-105">Especifica el estado de asignación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="a420e-105">Specifies the assignment status of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a420e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a420e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a420e-107">dispidTaskMode</span><span class="sxs-lookup"><span data-stu-id="a420e-107">dispidTaskMode</span></span>  <br/> |
|<span data-ttu-id="a420e-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="a420e-108">Property set:</span></span>  <br/> |<span data-ttu-id="a420e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a420e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a420e-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="a420e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a420e-111">0x00008518</span><span class="sxs-lookup"><span data-stu-id="a420e-111">0x00008518</span></span>  <br/> |
|<span data-ttu-id="a420e-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a420e-112">Data type:</span></span>  <br/> |<span data-ttu-id="a420e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a420e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a420e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="a420e-114">Area:</span></span>  <br/> |<span data-ttu-id="a420e-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="a420e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a420e-116">Notas</span><span class="sxs-lookup"><span data-stu-id="a420e-116">Remarks</span></span>

<span data-ttu-id="a420e-117">El valor debe ser una de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="a420e-117">The value must be one of the following.</span></span>
  
|<span data-ttu-id="a420e-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a420e-118">**Value**</span></span>|<span data-ttu-id="a420e-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a420e-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a420e-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a420e-120">0x00000000</span></span>  <br/> |<span data-ttu-id="a420e-121">No se asigna la tarea.</span><span class="sxs-lookup"><span data-stu-id="a420e-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="a420e-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a420e-122">0x00000001</span></span>  <br/> |<span data-ttu-id="a420e-123">La tarea está incrustada en una solicitud de tarea.</span><span class="sxs-lookup"><span data-stu-id="a420e-123">The task is embedded in a task request.</span></span>  <br/> |
|<span data-ttu-id="a420e-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a420e-124">0x00000002</span></span>  <br/> |<span data-ttu-id="a420e-125">La tarea se ha aceptado por el encargado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="a420e-125">The task was accepted by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="a420e-126">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="a420e-126">0x00000003</span></span>  <br/> |<span data-ttu-id="a420e-127">La tarea fue rechazada por el encargado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="a420e-127">The task was rejected by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="a420e-128">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="a420e-128">0x00000004</span></span>  <br/> |<span data-ttu-id="a420e-129">La tarea está incrustada en una actualización de la tarea.</span><span class="sxs-lookup"><span data-stu-id="a420e-129">The task is embedded in a task update.</span></span>  <br/> |
|<span data-ttu-id="a420e-130">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="a420e-130">0x00000005</span></span>  <br/> |<span data-ttu-id="a420e-131">Se asignó la tarea para el asignador de tareas.</span><span class="sxs-lookup"><span data-stu-id="a420e-131">The task was assigned to the task assigner.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a420e-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a420e-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a420e-133">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a420e-133">Protocol specifications</span></span>

<span data-ttu-id="a420e-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a420e-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a420e-135">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a420e-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a420e-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a420e-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a420e-137">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="a420e-137">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a420e-138">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a420e-138">Header files</span></span>

<span data-ttu-id="a420e-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a420e-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="a420e-140">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a420e-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a420e-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="a420e-141">See also</span></span>



[<span data-ttu-id="a420e-142">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a420e-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a420e-143">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a420e-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a420e-144">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="a420e-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a420e-145">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a420e-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

