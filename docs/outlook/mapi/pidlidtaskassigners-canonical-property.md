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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385077"
---
# <a name="pidlidtaskassigners-canonical-property"></a><span data-ttu-id="da060-103">Propiedad canónica PidLidTaskAssigners</span><span class="sxs-lookup"><span data-stu-id="da060-103">PidLidTaskAssigners Canonical Property</span></span>

  
  
<span data-ttu-id="da060-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da060-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da060-105">Contiene una pila de las entradas que representan a assigners de tarea.</span><span class="sxs-lookup"><span data-stu-id="da060-105">Contains a stack of entries that represent task assigners.</span></span> <span data-ttu-id="da060-106">El asignador de tareas más reciente aparece en la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="da060-106">The most recent task assigner appears at the top of the stack.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="da060-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="da060-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="da060-108">dispidTaskMyDelegators</span><span class="sxs-lookup"><span data-stu-id="da060-108">dispidTaskMyDelegators</span></span>  <br/> |
|<span data-ttu-id="da060-109">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="da060-109">Property set:</span></span>  <br/> |<span data-ttu-id="da060-110">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="da060-110">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="da060-111">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="da060-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="da060-112">0x00008117</span><span class="sxs-lookup"><span data-stu-id="da060-112">0x00008117</span></span>  <br/> |
|<span data-ttu-id="da060-113">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="da060-113">Data type:</span></span>  <br/> |<span data-ttu-id="da060-114">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="da060-114">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="da060-115">Área:</span><span class="sxs-lookup"><span data-stu-id="da060-115">Area:</span></span>  <br/> |<span data-ttu-id="da060-116">Task</span><span class="sxs-lookup"><span data-stu-id="da060-116">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da060-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="da060-117">Remarks</span></span>

<span data-ttu-id="da060-118">Cuando el cliente recibe una solicitud de tarea, anexa a esta propiedad, la estructura que se define en [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), una entrada que representa el remitente de la tarea.</span><span class="sxs-lookup"><span data-stu-id="da060-118">When the client receives a task request, it appends to this property, which structure is defined in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), an entry that represents the task's sender.</span></span> <span data-ttu-id="da060-119">Cuando el cliente recibe un rechazo de la tarea, el cliente quita la última entrada asignador de tareas de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="da060-119">When the client receives a task rejection, the client removes the last task assigner entry from this property.</span></span> <span data-ttu-id="da060-120">Cuando el cliente envía una respuesta de tarea, en el cliente se envía a la última asignador de tareas que aparecen en el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="da060-120">When the client sends a task response, the client sends it to the last task assigner listed in the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="da060-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="da060-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="da060-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="da060-122">Protocol specifications</span></span>

<span data-ttu-id="da060-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da060-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da060-124">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="da060-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="da060-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da060-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da060-126">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas</span><span class="sxs-lookup"><span data-stu-id="da060-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="da060-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="da060-127">Header files</span></span>

<span data-ttu-id="da060-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="da060-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="da060-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="da060-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="da060-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="da060-130">See also</span></span>



[<span data-ttu-id="da060-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="da060-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="da060-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="da060-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="da060-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="da060-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="da060-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="da060-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

