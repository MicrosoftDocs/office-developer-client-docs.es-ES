---
title: Propiedad canónico PidLidTaskFRecurring
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: eb97d278640b4cdd2b14152bf4745f883fe2edba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818958"
---
# <a name="pidlidtaskfrecurring-canonical-property"></a><span data-ttu-id="0f391-103">Propiedad canónico PidLidTaskFRecurring</span><span class="sxs-lookup"><span data-stu-id="0f391-103">PidLidTaskFRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="0f391-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0f391-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0f391-105">Indica si la tarea incluye un patrón de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="0f391-105">Indicates whether the task includes a recurrence pattern.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0f391-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0f391-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f391-107">dispidTaskFRecur</span><span class="sxs-lookup"><span data-stu-id="0f391-107">dispidTaskFRecur</span></span>  <br/> |
|<span data-ttu-id="0f391-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="0f391-108">Property set:</span></span>  <br/> |<span data-ttu-id="0f391-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="0f391-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="0f391-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="0f391-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0f391-111">0x00008126</span><span class="sxs-lookup"><span data-stu-id="0f391-111">0x00008126</span></span>  <br/> |
|<span data-ttu-id="0f391-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0f391-112">Data type:</span></span>  <br/> |<span data-ttu-id="0f391-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0f391-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0f391-114">Área:</span><span class="sxs-lookup"><span data-stu-id="0f391-114">Area:</span></span>  <br/> |<span data-ttu-id="0f391-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="0f391-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f391-116">Notas</span><span class="sxs-lookup"><span data-stu-id="0f391-116">Remarks</span></span>

<span data-ttu-id="0f391-117">Si esta propiedad se deja sin establecer, se supone un valor predeterminado de FALSE.</span><span class="sxs-lookup"><span data-stu-id="0f391-117">If this property is left unset, a default value of FALSE is assumed.</span></span> <span data-ttu-id="0f391-118">Si se establece en TRUE, la **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) y también se deben establecer las propiedades de **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) como se especifica en [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0f391-118">If it is set to TRUE, the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) and **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) properties must also be set as specified in [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0f391-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f391-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0f391-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0f391-120">Protocol specifications</span></span>

<span data-ttu-id="0f391-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f391-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f391-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0f391-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0f391-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f391-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f391-124">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="0f391-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0f391-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0f391-125">Header files</span></span>

<span data-ttu-id="0f391-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f391-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f391-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0f391-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f391-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="0f391-128">See also</span></span>



[<span data-ttu-id="0f391-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0f391-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f391-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0f391-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f391-131">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="0f391-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f391-132">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0f391-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

