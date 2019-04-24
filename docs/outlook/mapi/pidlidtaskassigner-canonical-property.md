---
title: Propiedad canónica PidLidTaskAssigner
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigner
api_type:
- COM
ms.assetid: f7047e4e-0fb3-476b-9568-8f1135e6d970
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ef5f78fa36632227311d037ee61085c677920fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340092"
---
# <a name="pidlidtaskassigner-canonical-property"></a><span data-ttu-id="9988b-103">Propiedad canónica PidLidTaskAssigner</span><span class="sxs-lookup"><span data-stu-id="9988b-103">PidLidTaskAssigner Canonical Property</span></span>

  
  
<span data-ttu-id="9988b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9988b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9988b-105">Nombra el último usuario al que se asignó la tarea por última vez.</span><span class="sxs-lookup"><span data-stu-id="9988b-105">Names the user who was last assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9988b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9988b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9988b-107">dispidTaskDelegator</span><span class="sxs-lookup"><span data-stu-id="9988b-107">dispidTaskDelegator</span></span>  <br/> |
|<span data-ttu-id="9988b-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="9988b-108">Property set:</span></span>  <br/> |<span data-ttu-id="9988b-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="9988b-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="9988b-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="9988b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9988b-111">0x00008121</span><span class="sxs-lookup"><span data-stu-id="9988b-111">0x00008121</span></span>  <br/> |
|<span data-ttu-id="9988b-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9988b-112">Data type:</span></span>  <br/> |<span data-ttu-id="9988b-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9988b-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9988b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="9988b-114">Area:</span></span>  <br/> |<span data-ttu-id="9988b-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="9988b-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9988b-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9988b-116">Remarks</span></span>

<span data-ttu-id="9988b-117">Si no se ha asignado la tarea, esta propiedad se deja sin establecer.</span><span class="sxs-lookup"><span data-stu-id="9988b-117">If the task has not been assigned, this property is left unset.</span></span> <span data-ttu-id="9988b-118">Dado que el cliente establece esta propiedad después de que el usuario al que se le asigna una tarea recibe una solicitud de tarea, la propiedad no se establecerá en la copia de la tarea del asignador de tarea.</span><span class="sxs-lookup"><span data-stu-id="9988b-118">Because the client sets this property after the task assignee receives a task request, the property will not be set on the task assigner's copy of the task.</span></span> <span data-ttu-id="9988b-119">Cuando el cliente agrega o quita un asignador de tareas de la lista de asignaciones de tareas en la propiedad **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)), la propiedad **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) debe establecerse en el valor agregado o se ha quitado el asignador de tareas.</span><span class="sxs-lookup"><span data-stu-id="9988b-119">When the client adds or removes a task assigner from the task assigner list in the **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)) property, the **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) property must be set to the added or removed task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9988b-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9988b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9988b-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="9988b-121">Protocol specifications</span></span>

<span data-ttu-id="9988b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9988b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9988b-123">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9988b-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9988b-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9988b-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9988b-125">Define varios objetos que modelan el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="9988b-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9988b-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9988b-126">Header files</span></span>

<span data-ttu-id="9988b-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9988b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="9988b-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9988b-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9988b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9988b-129">See also</span></span>



[<span data-ttu-id="9988b-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9988b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9988b-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="9988b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9988b-132">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9988b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9988b-133">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="9988b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

