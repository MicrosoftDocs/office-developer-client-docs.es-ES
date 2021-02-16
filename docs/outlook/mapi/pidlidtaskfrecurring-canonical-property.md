---
title: Propiedad canónica PidLidTaskFRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFRecurring
api_type:
- COM
ms.assetid: 47c9ccbb-161c-4829-8ffb-201f3b54cd45
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: aec9dd328e802e185c870d3ecd94cbd1d10ac67d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303055"
---
# <a name="pidlidtaskfrecurring-canonical-property"></a><span data-ttu-id="aa94c-103">Propiedad canónica PidLidTaskFRecurring</span><span class="sxs-lookup"><span data-stu-id="aa94c-103">PidLidTaskFRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="aa94c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa94c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa94c-105">Indica si la tarea incluye un patrón de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="aa94c-105">Indicates whether the task includes a recurrence pattern.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aa94c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="aa94c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aa94c-107">dispidTaskFRecur</span><span class="sxs-lookup"><span data-stu-id="aa94c-107">dispidTaskFRecur</span></span>  <br/> |
|<span data-ttu-id="aa94c-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="aa94c-108">Property set:</span></span>  <br/> |<span data-ttu-id="aa94c-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="aa94c-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="aa94c-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="aa94c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="aa94c-111">0x00008126</span><span class="sxs-lookup"><span data-stu-id="aa94c-111">0x00008126</span></span>  <br/> |
|<span data-ttu-id="aa94c-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="aa94c-112">Data type:</span></span>  <br/> |<span data-ttu-id="aa94c-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="aa94c-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="aa94c-114">Área:</span><span class="sxs-lookup"><span data-stu-id="aa94c-114">Area:</span></span>  <br/> |<span data-ttu-id="aa94c-115">Task</span><span class="sxs-lookup"><span data-stu-id="aa94c-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa94c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aa94c-116">Remarks</span></span>

<span data-ttu-id="aa94c-117">Si esta propiedad se deja sin conjunto, se supone un valor predeterminado de FALSE.</span><span class="sxs-lookup"><span data-stu-id="aa94c-117">If this property is left unset, a default value of FALSE is assumed.</span></span> <span data-ttu-id="aa94c-118">Si se establece en TRUE, las propiedades **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) y **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) también deben establecerse como se especifica en [[MS-OCCITASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="aa94c-118">If it is set to TRUE, the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) and **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) properties must also be set as specified in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aa94c-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa94c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aa94c-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="aa94c-120">Protocol specifications</span></span>

<span data-ttu-id="aa94c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa94c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aa94c-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="aa94c-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aa94c-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa94c-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aa94c-124">Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="aa94c-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aa94c-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="aa94c-125">Header files</span></span>

<span data-ttu-id="aa94c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aa94c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="aa94c-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="aa94c-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aa94c-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="aa94c-128">See also</span></span>



[<span data-ttu-id="aa94c-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="aa94c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aa94c-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="aa94c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aa94c-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="aa94c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aa94c-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="aa94c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

