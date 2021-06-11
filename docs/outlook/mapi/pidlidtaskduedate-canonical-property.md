---
title: Propiedad canónica PidLidTaskDueDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDueDate
api_type:
- COM
ms.assetid: 69ed3d48-3741-4a9a-8f98-51382b850c27
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2e21d164cbb9403d3fa1dc05cf474359a517d64b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303328"
---
# <a name="pidlidtaskduedate-canonical-property"></a><span data-ttu-id="7f522-103">Propiedad canónica PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="7f522-103">PidLidTaskDueDate Canonical Property</span></span>

  
  
<span data-ttu-id="7f522-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f522-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f522-105">Representa la fecha en que el usuario espera completar la tarea.</span><span class="sxs-lookup"><span data-stu-id="7f522-105">Represents the date when the user expects to complete the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f522-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7f522-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f522-107">dispidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="7f522-107">dispidTaskDueDate</span></span>  <br/> |
|<span data-ttu-id="7f522-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="7f522-108">Property set:</span></span>  <br/> |<span data-ttu-id="7f522-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="7f522-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="7f522-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="7f522-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7f522-111">0x00008105</span><span class="sxs-lookup"><span data-stu-id="7f522-111">0x00008105</span></span>  <br/> |
|<span data-ttu-id="7f522-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7f522-112">Data type:</span></span>  <br/> |<span data-ttu-id="7f522-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="7f522-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="7f522-114">Área:</span><span class="sxs-lookup"><span data-stu-id="7f522-114">Area:</span></span>  <br/> |<span data-ttu-id="7f522-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="7f522-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f522-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7f522-116">Remarks</span></span>

<span data-ttu-id="7f522-117">La tarea no tiene fecha de vencimiento si esta propiedad no está establecida o se establece en 0x5AE980E0 (1.525.252.320).</span><span class="sxs-lookup"><span data-stu-id="7f522-117">The task has no due date if this property is unset or set to 0x5AE980E0 (1,525,252,320).</span></span> <span data-ttu-id="7f522-118">Sin embargo, una fecha de vencimiento es opcional solo si no se indica ninguna fecha de inicio en la **propiedad dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7f522-118">However, a due date is optional only if no start date is indicated in the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span> <span data-ttu-id="7f522-119">Si la tarea tiene una fecha de vencimiento, el valor debe tener un componente de hora de medianoche y la propiedad **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) también debe establecerse.</span><span class="sxs-lookup"><span data-stu-id="7f522-119">If the task has a due date, the value must have a time component of midnight, and the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="7f522-120">Si **dispidTaskStartDate** tiene una fecha de inicio, el valor de la propiedad **dispidTaskDueDate** debe ser mayor o igual que el valor de **dispidTaskStartDate**.</span><span class="sxs-lookup"><span data-stu-id="7f522-120">If **dispidTaskStartDate** has a start date, then the value of the **dispidTaskDueDate** property must be greater than or equal to the value of **dispidTaskStartDate**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7f522-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f522-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7f522-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="7f522-122">Protocol specifications</span></span>

<span data-ttu-id="7f522-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f522-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f522-124">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="7f522-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7f522-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f522-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f522-126">Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="7f522-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="7f522-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f522-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f522-128">Especifica las propiedades y el modelo de interacción para el correo electrónico y otros avisos de objetos.</span><span class="sxs-lookup"><span data-stu-id="7f522-128">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7f522-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7f522-129">Header files</span></span>

<span data-ttu-id="7f522-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7f522-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f522-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7f522-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f522-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f522-132">See also</span></span>



[<span data-ttu-id="7f522-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7f522-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f522-134">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7f522-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f522-135">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7f522-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f522-136">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="7f522-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

