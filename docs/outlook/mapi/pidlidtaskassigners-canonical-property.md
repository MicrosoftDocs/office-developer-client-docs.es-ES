---
title: Propiedad canónico PidLidTaskAssigners
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 89e0b6eae35de9e40dba411afb82e19aa81fb635
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818937"
---
# <a name="pidlidtaskassigners-canonical-property"></a><span data-ttu-id="f28f6-103">Propiedad canónico PidLidTaskAssigners</span><span class="sxs-lookup"><span data-stu-id="f28f6-103">PidLidTaskAssigners Canonical Property</span></span>

  
  
<span data-ttu-id="f28f6-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f28f6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f28f6-105">Contiene una pila de las entradas que representan a assigners de tarea.</span><span class="sxs-lookup"><span data-stu-id="f28f6-105">Contains a stack of entries that represent task assigners.</span></span> <span data-ttu-id="f28f6-106">El asignador de tareas más reciente aparece en la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="f28f6-106">The most recent task assigner appears at the top of the stack.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f28f6-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f28f6-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="f28f6-108">dispidTaskMyDelegators</span><span class="sxs-lookup"><span data-stu-id="f28f6-108">dispidTaskMyDelegators</span></span>  <br/> |
|<span data-ttu-id="f28f6-109">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="f28f6-109">Property set:</span></span>  <br/> |<span data-ttu-id="f28f6-110">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="f28f6-110">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="f28f6-111">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="f28f6-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f28f6-112">0x00008117</span><span class="sxs-lookup"><span data-stu-id="f28f6-112">0x00008117</span></span>  <br/> |
|<span data-ttu-id="f28f6-113">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f28f6-113">Data type:</span></span>  <br/> |<span data-ttu-id="f28f6-114">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f28f6-114">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f28f6-115">Área:</span><span class="sxs-lookup"><span data-stu-id="f28f6-115">Area:</span></span>  <br/> |<span data-ttu-id="f28f6-116">Tarea</span><span class="sxs-lookup"><span data-stu-id="f28f6-116">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f28f6-117">Notas</span><span class="sxs-lookup"><span data-stu-id="f28f6-117">Remarks</span></span>

<span data-ttu-id="f28f6-118">Cuando el cliente recibe una solicitud de tarea, anexa a esta propiedad, la estructura que se define en [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), una entrada que representa el remitente de la tarea.</span><span class="sxs-lookup"><span data-stu-id="f28f6-118">When the client receives a task request, it appends to this property, which structure is defined in [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), an entry that represents the task's sender.</span></span> <span data-ttu-id="f28f6-119">Cuando el cliente recibe un rechazo de la tarea, el cliente quita la última entrada asignador de tareas de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f28f6-119">When the client receives a task rejection, the client removes the last task assigner entry from this property.</span></span> <span data-ttu-id="f28f6-120">Cuando el cliente envía una respuesta de tarea, en el cliente se envía a la última asignador de tareas que aparecen en el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f28f6-120">When the client sends a task response, the client sends it to the last task assigner listed in the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f28f6-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f28f6-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f28f6-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f28f6-122">Protocol specifications</span></span>

<span data-ttu-id="f28f6-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f28f6-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f28f6-124">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f28f6-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f28f6-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f28f6-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f28f6-126">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas</span><span class="sxs-lookup"><span data-stu-id="f28f6-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="f28f6-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f28f6-127">Header files</span></span>

<span data-ttu-id="f28f6-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f28f6-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="f28f6-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f28f6-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f28f6-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="f28f6-130">See also</span></span>



[<span data-ttu-id="f28f6-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f28f6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f28f6-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f28f6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f28f6-133">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="f28f6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f28f6-134">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f28f6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

