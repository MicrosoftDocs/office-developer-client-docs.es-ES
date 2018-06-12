---
title: Propiedad canónico PidLidTaskDueDate
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: d26a686573a9dc178a46b7dfdc5c18485303b7ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818971"
---
# <a name="pidlidtaskduedate-canonical-property"></a><span data-ttu-id="a9e25-103">Propiedad canónico PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="a9e25-103">PidLidTaskDueDate Canonical Property</span></span>

  
  
<span data-ttu-id="a9e25-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a9e25-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a9e25-105">Representa la fecha cuando el usuario espera para completar la tarea.</span><span class="sxs-lookup"><span data-stu-id="a9e25-105">Represents the date when the user expects to complete the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a9e25-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a9e25-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a9e25-107">dispidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="a9e25-107">dispidTaskDueDate</span></span>  <br/> |
|<span data-ttu-id="a9e25-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="a9e25-108">Property set:</span></span>  <br/> |<span data-ttu-id="a9e25-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="a9e25-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="a9e25-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="a9e25-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a9e25-111">0x00008105</span><span class="sxs-lookup"><span data-stu-id="a9e25-111">0x00008105</span></span>  <br/> |
|<span data-ttu-id="a9e25-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a9e25-112">Data type:</span></span>  <br/> |<span data-ttu-id="a9e25-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a9e25-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="a9e25-114">Área:</span><span class="sxs-lookup"><span data-stu-id="a9e25-114">Area:</span></span>  <br/> |<span data-ttu-id="a9e25-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="a9e25-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9e25-116">Notas</span><span class="sxs-lookup"><span data-stu-id="a9e25-116">Remarks</span></span>

<span data-ttu-id="a9e25-117">La tarea no tiene ninguna fecha de vencimiento si esta propiedad está sin establecer ni establecer a 0x5AE980E0 (1,525,252,320).</span><span class="sxs-lookup"><span data-stu-id="a9e25-117">The task has no due date if this property is unset or set to 0x5AE980E0 (1,525,252,320).</span></span> <span data-ttu-id="a9e25-118">Sin embargo, una fecha de vencimiento es opcional sólo si no hay fecha de inicio se indica en la propiedad **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a9e25-118">However, a due date is optional only if no start date is indicated in the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span> <span data-ttu-id="a9e25-119">Si la tarea tiene una fecha de vencimiento, el valor debe tener un componente de hora de la medianoche, y también se debe establecer la propiedad **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a9e25-119">If the task has a due date, the value must have a time component of midnight, and the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="a9e25-120">Si **dispidTaskStartDate** tiene una fecha de inicio, el valor de la propiedad **dispidTaskDueDate** debe ser mayor o igual que el valor de **dispidTaskStartDate**.</span><span class="sxs-lookup"><span data-stu-id="a9e25-120">If **dispidTaskStartDate** has a start date, then the value of the **dispidTaskDueDate** property must be greater than or equal to the value of **dispidTaskStartDate**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a9e25-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a9e25-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a9e25-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a9e25-122">Protocol specifications</span></span>

<span data-ttu-id="a9e25-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9e25-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9e25-124">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a9e25-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a9e25-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9e25-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9e25-126">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="a9e25-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="a9e25-127">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9e25-127">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9e25-128">Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.</span><span class="sxs-lookup"><span data-stu-id="a9e25-128">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a9e25-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a9e25-129">Header files</span></span>

<span data-ttu-id="a9e25-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a9e25-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="a9e25-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a9e25-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a9e25-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="a9e25-132">See also</span></span>



[<span data-ttu-id="a9e25-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a9e25-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a9e25-134">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a9e25-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a9e25-135">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="a9e25-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a9e25-136">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a9e25-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

