---
title: Propiedad canónica PidLidTaskStartDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStartDate
api_type:
- COM
ms.assetid: fe87eb3d-21d1-45bb-b848-e141ce1be6a0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3bc475292e47a9ad8dd9565e17640ef95e7b3c76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316684"
---
# <a name="pidlidtaskstartdate-canonical-property"></a><span data-ttu-id="84e63-103">Propiedad canónica PidLidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="84e63-103">PidLidTaskStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="84e63-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84e63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84e63-105">La fecha en la que el usuario espera comenzar la tarea.</span><span class="sxs-lookup"><span data-stu-id="84e63-105">The date when the user expects to begin the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="84e63-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="84e63-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84e63-107">dispidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="84e63-107">dispidTaskStartDate</span></span>  <br/> |
|<span data-ttu-id="84e63-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="84e63-108">Property set:</span></span>  <br/> |<span data-ttu-id="84e63-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="84e63-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="84e63-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="84e63-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="84e63-111">0x00008104</span><span class="sxs-lookup"><span data-stu-id="84e63-111">0x00008104</span></span>  <br/> |
|<span data-ttu-id="84e63-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="84e63-112">Data type:</span></span>  <br/> |<span data-ttu-id="84e63-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="84e63-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="84e63-114">Área:</span><span class="sxs-lookup"><span data-stu-id="84e63-114">Area:</span></span>  <br/> |<span data-ttu-id="84e63-115">Task</span><span class="sxs-lookup"><span data-stu-id="84e63-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84e63-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="84e63-116">Remarks</span></span>

<span data-ttu-id="84e63-117">Si este valor de propiedad se deja sin conjunto, la tarea no tiene una fecha de inicio.</span><span class="sxs-lookup"><span data-stu-id="84e63-117">If this property value is left unset, the task does not have a start date.</span></span> <span data-ttu-id="84e63-118">Un valor de "0x5AE980E0" (1.525.252.320) también significa que la tarea no tiene una fecha de inicio.</span><span class="sxs-lookup"><span data-stu-id="84e63-118">A value of "0x5AE980E0" (1,525,252,320) also means that the task does not have a start date.</span></span> <span data-ttu-id="84e63-119">Si la tarea tiene una fecha de inicio, el valor debe tener un componente de hora de medianoche y también deben establecerse las propiedades **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) y **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="84e63-119">If the task has a start date, the value must have a time component of midnight, and the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) and **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) properties must also be set.</span></span>
  
<span data-ttu-id="84e63-120">Esta propiedad se comparte mediante la especificación del protocolo de marcación informativo y Task-Related especificación del protocolo de objetos que se encuentra en [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="84e63-120">This property is shared by the Informational Flagging Protocol Specification and Task-Related Object Protocol Specification located in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="84e63-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="84e63-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84e63-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="84e63-122">Protocol specifications</span></span>

<span data-ttu-id="84e63-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84e63-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84e63-124">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="84e63-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="84e63-125">[[MS-OJOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84e63-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84e63-126">Especifica las propiedades y operaciones permitidas en los contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="84e63-126">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84e63-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="84e63-127">Header files</span></span>

<span data-ttu-id="84e63-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84e63-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="84e63-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="84e63-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84e63-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="84e63-130">See also</span></span>



[<span data-ttu-id="84e63-131">Propiedad can�nico de PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="84e63-131">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
  
[<span data-ttu-id="84e63-132">Propiedad can�nico de PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="84e63-132">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)


[<span data-ttu-id="84e63-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="84e63-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84e63-134">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="84e63-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84e63-135">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="84e63-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84e63-136">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="84e63-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

