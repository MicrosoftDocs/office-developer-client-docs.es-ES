---
title: Propiedad canónico PidLidTaskAssigner
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 5b711b1e0db0fab93016d3f1c979d81a142c9946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818949"
---
# <a name="pidlidtaskassigner-canonical-property"></a><span data-ttu-id="fd54e-103">Propiedad canónico PidLidTaskAssigner</span><span class="sxs-lookup"><span data-stu-id="fd54e-103">PidLidTaskAssigner Canonical Property</span></span>

  
  
<span data-ttu-id="fd54e-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd54e-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="fd54e-105">Los nombres de usuario que por última vez asignado la tarea.</span><span class="sxs-lookup"><span data-stu-id="fd54e-105">Names the user who was last assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd54e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fd54e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fd54e-107">dispidTaskDelegator</span><span class="sxs-lookup"><span data-stu-id="fd54e-107">dispidTaskDelegator</span></span>  <br/> |
|<span data-ttu-id="fd54e-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="fd54e-108">Property set:</span></span>  <br/> |<span data-ttu-id="fd54e-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="fd54e-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="fd54e-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="fd54e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fd54e-111">0x00008121</span><span class="sxs-lookup"><span data-stu-id="fd54e-111">0x00008121</span></span>  <br/> |
|<span data-ttu-id="fd54e-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fd54e-112">Data type:</span></span>  <br/> |<span data-ttu-id="fd54e-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fd54e-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fd54e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="fd54e-114">Area:</span></span>  <br/> |<span data-ttu-id="fd54e-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="fd54e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd54e-116">Notas</span><span class="sxs-lookup"><span data-stu-id="fd54e-116">Remarks</span></span>

<span data-ttu-id="fd54e-117">Si no se ha asignado la tarea, esta propiedad se deja sin establecer.</span><span class="sxs-lookup"><span data-stu-id="fd54e-117">If the task has not been assigned, this property is left unset.</span></span> <span data-ttu-id="fd54e-118">Debido a que el cliente establece esta propiedad una vez que el encargado de la tarea recibe una solicitud de tarea, la propiedad no se establecerá en la copia del asignador de tarea de la tarea.</span><span class="sxs-lookup"><span data-stu-id="fd54e-118">Because the client sets this property after the task assignee receives a task request, the property will not be set on the task assigner's copy of the task.</span></span> <span data-ttu-id="fd54e-119">Cuando el cliente agrega o quita a un asignador de tarea de la lista de asignador de tareas en la propiedad **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)), la propiedad **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) debe ser establecida en el agregado o asignador de tarea se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="fd54e-119">When the client adds or removes a task assigner from the task assigner list in the **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)) property, the **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) property must be set to the added or removed task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fd54e-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd54e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fd54e-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="fd54e-121">Protocol specifications</span></span>

<span data-ttu-id="fd54e-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd54e-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd54e-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fd54e-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fd54e-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd54e-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd54e-125">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="fd54e-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fd54e-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fd54e-126">Header files</span></span>

<span data-ttu-id="fd54e-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fd54e-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="fd54e-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fd54e-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd54e-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="fd54e-129">See also</span></span>



[<span data-ttu-id="fd54e-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fd54e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fd54e-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="fd54e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fd54e-132">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="fd54e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fd54e-133">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fd54e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

