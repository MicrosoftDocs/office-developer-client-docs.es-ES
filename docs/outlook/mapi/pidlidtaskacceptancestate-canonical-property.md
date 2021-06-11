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
ms.openlocfilehash: b42be4b42d085aba8999a8c3f1a780ed972fa136
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331293"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a><span data-ttu-id="422c9-103">Propiedad canónica PidLidTaskAcceptanceState</span><span class="sxs-lookup"><span data-stu-id="422c9-103">PidLidTaskAcceptanceState Canonical Property</span></span>

  
  
<span data-ttu-id="422c9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="422c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="422c9-105">Indica el estado de aceptación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="422c9-105">Indicates the acceptance state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="422c9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="422c9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="422c9-107">dispidTaskDelegValue</span><span class="sxs-lookup"><span data-stu-id="422c9-107">dispidTaskDelegValue</span></span>  <br/> |
|<span data-ttu-id="422c9-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="422c9-108">Property set:</span></span>  <br/> |<span data-ttu-id="422c9-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="422c9-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="422c9-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="422c9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="422c9-111">0x0000812A</span><span class="sxs-lookup"><span data-stu-id="422c9-111">0x0000812A</span></span>  <br/> |
|<span data-ttu-id="422c9-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="422c9-112">Data type:</span></span>  <br/> |<span data-ttu-id="422c9-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="422c9-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="422c9-114">Área:</span><span class="sxs-lookup"><span data-stu-id="422c9-114">Area:</span></span>  <br/> |<span data-ttu-id="422c9-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="422c9-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="422c9-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="422c9-116">Remarks</span></span>

<span data-ttu-id="422c9-117">En la tabla siguiente se muestran los valores posibles para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="422c9-117">The following table shows the possible values for this property.</span></span>
  
|<span data-ttu-id="422c9-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="422c9-118">**Value**</span></span>|<span data-ttu-id="422c9-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="422c9-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="422c9-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="422c9-120">0x00000000</span></span>  <br/> |<span data-ttu-id="422c9-121">La tarea no está asignada.</span><span class="sxs-lookup"><span data-stu-id="422c9-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="422c9-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="422c9-122">0x00000001</span></span>  <br/> |<span data-ttu-id="422c9-123">El estado de aceptación de la tarea es desconocido.</span><span class="sxs-lookup"><span data-stu-id="422c9-123">The task's acceptance status is unknown.</span></span>  <br/> |
|<span data-ttu-id="422c9-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="422c9-124">0x00000002</span></span>  <br/> |<span data-ttu-id="422c9-125">El destinatario de la tarea aceptó la tarea.</span><span class="sxs-lookup"><span data-stu-id="422c9-125">The task assignee accepted the task.</span></span> <span data-ttu-id="422c9-126">Este valor se establece cuando el cliente procesa la aceptación de una tarea.</span><span class="sxs-lookup"><span data-stu-id="422c9-126">This value is set when the client processes a task acceptance.</span></span>  <br/> |
|<span data-ttu-id="422c9-127">0x00000003</span><span class="sxs-lookup"><span data-stu-id="422c9-127">0x00000003</span></span>  <br/> |<span data-ttu-id="422c9-128">El destinatario de la tarea rechazó la tarea.</span><span class="sxs-lookup"><span data-stu-id="422c9-128">The task assignee rejected the task.</span></span> <span data-ttu-id="422c9-129">Este valor se establece cuando el cliente procesa un rechazo de tarea.</span><span class="sxs-lookup"><span data-stu-id="422c9-129">This value is set when the client processes a task rejection.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="422c9-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="422c9-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="422c9-131">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="422c9-131">Protocol specifications</span></span>

<span data-ttu-id="422c9-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="422c9-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="422c9-133">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="422c9-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="422c9-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="422c9-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="422c9-135">Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="422c9-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="422c9-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="422c9-136">Header files</span></span>

<span data-ttu-id="422c9-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="422c9-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="422c9-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="422c9-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="422c9-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="422c9-139">See also</span></span>



[<span data-ttu-id="422c9-140">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="422c9-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="422c9-141">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="422c9-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="422c9-142">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="422c9-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="422c9-143">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="422c9-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

