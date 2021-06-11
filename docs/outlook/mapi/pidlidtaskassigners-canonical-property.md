---
title: Propiedad canónica PidLidTaskAssigners
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigners
api_type:
- COM
ms.assetid: 07500bd0-bcff-4b03-8ed3-80508875e253
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 97a4915d5422f6c5463ed399835172725b83407f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303069"
---
# <a name="pidlidtaskassigners-canonical-property"></a><span data-ttu-id="7675c-103">Propiedad canónica PidLidTaskAssigners</span><span class="sxs-lookup"><span data-stu-id="7675c-103">PidLidTaskAssigners Canonical Property</span></span>

  
  
<span data-ttu-id="7675c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7675c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7675c-105">Contiene una pila de entradas que representan a los asignadores de tareas.</span><span class="sxs-lookup"><span data-stu-id="7675c-105">Contains a stack of entries that represent task assigners.</span></span> <span data-ttu-id="7675c-106">El asignador de tareas más reciente aparece en la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="7675c-106">The most recent task assigner appears at the top of the stack.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7675c-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7675c-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="7675c-108">dispidTaskMyDelegators</span><span class="sxs-lookup"><span data-stu-id="7675c-108">dispidTaskMyDelegators</span></span>  <br/> |
|<span data-ttu-id="7675c-109">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="7675c-109">Property set:</span></span>  <br/> |<span data-ttu-id="7675c-110">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="7675c-110">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="7675c-111">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="7675c-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7675c-112">0x00008117</span><span class="sxs-lookup"><span data-stu-id="7675c-112">0x00008117</span></span>  <br/> |
|<span data-ttu-id="7675c-113">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7675c-113">Data type:</span></span>  <br/> |<span data-ttu-id="7675c-114">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7675c-114">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7675c-115">Área:</span><span class="sxs-lookup"><span data-stu-id="7675c-115">Area:</span></span>  <br/> |<span data-ttu-id="7675c-116">Tarea</span><span class="sxs-lookup"><span data-stu-id="7675c-116">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7675c-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7675c-117">Remarks</span></span>

<span data-ttu-id="7675c-118">Cuando el cliente recibe una solicitud de tarea, se anexa a esta propiedad, cuya estructura se define en [[MS-OXOTASK],](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)una entrada que representa al remitente de la tarea.</span><span class="sxs-lookup"><span data-stu-id="7675c-118">When the client receives a task request, it appends to this property, which structure is defined in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), an entry that represents the task's sender.</span></span> <span data-ttu-id="7675c-119">Cuando el cliente recibe un rechazo de tarea, el cliente quita la última entrada del asignador de tareas de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="7675c-119">When the client receives a task rejection, the client removes the last task assigner entry from this property.</span></span> <span data-ttu-id="7675c-120">Cuando el cliente envía una respuesta de tarea, el cliente la envía al último asignador de tareas que aparece en el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="7675c-120">When the client sends a task response, the client sends it to the last task assigner listed in the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7675c-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7675c-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7675c-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="7675c-122">Protocol specifications</span></span>

<span data-ttu-id="7675c-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7675c-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7675c-124">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="7675c-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7675c-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7675c-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7675c-126">Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas</span><span class="sxs-lookup"><span data-stu-id="7675c-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="7675c-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7675c-127">Header files</span></span>

<span data-ttu-id="7675c-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7675c-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="7675c-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7675c-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7675c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="7675c-130">See also</span></span>



[<span data-ttu-id="7675c-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7675c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7675c-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7675c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7675c-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7675c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7675c-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="7675c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

