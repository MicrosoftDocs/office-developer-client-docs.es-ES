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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383530"
---
# <a name="pidlidtaskstartdate-canonical-property"></a><span data-ttu-id="d1b83-103">Propiedad canónica PidLidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="d1b83-103">PidLidTaskStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="d1b83-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1b83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1b83-105">La fecha cuando el usuario espera para comenzar la tarea.</span><span class="sxs-lookup"><span data-stu-id="d1b83-105">The date when the user expects to begin the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1b83-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d1b83-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1b83-107">dispidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="d1b83-107">dispidTaskStartDate</span></span>  <br/> |
|<span data-ttu-id="d1b83-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="d1b83-108">Property set:</span></span>  <br/> |<span data-ttu-id="d1b83-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="d1b83-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="d1b83-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="d1b83-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d1b83-111">0x00008104</span><span class="sxs-lookup"><span data-stu-id="d1b83-111">0x00008104</span></span>  <br/> |
|<span data-ttu-id="d1b83-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d1b83-112">Data type:</span></span>  <br/> |<span data-ttu-id="d1b83-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d1b83-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d1b83-114">Área:</span><span class="sxs-lookup"><span data-stu-id="d1b83-114">Area:</span></span>  <br/> |<span data-ttu-id="d1b83-115">Task</span><span class="sxs-lookup"><span data-stu-id="d1b83-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1b83-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d1b83-116">Remarks</span></span>

<span data-ttu-id="d1b83-117">Si el valor de esta propiedad se deja sin establecer, la tarea no tiene una fecha de inicio.</span><span class="sxs-lookup"><span data-stu-id="d1b83-117">If this property value is left unset, the task does not have a start date.</span></span> <span data-ttu-id="d1b83-118">Un valor de "0x5AE980E0" (1,525,252,320) también significa que la tarea no tiene una fecha de inicio.</span><span class="sxs-lookup"><span data-stu-id="d1b83-118">A value of "0x5AE980E0" (1,525,252,320) also means that the task does not have a start date.</span></span> <span data-ttu-id="d1b83-119">Si la tarea tiene una fecha de inicio, el valor debe tener un componente de hora de la medianoche, y también se deben establecer las propiedades de **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) y **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d1b83-119">If the task has a start date, the value must have a time component of midnight, and the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) and **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) properties must also be set.</span></span>
  
<span data-ttu-id="d1b83-120">Esta propiedad se comparte con la especificación de protocolo informativo marcar y especificación del protocolo Task-Related objeto que se encuentra en [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d1b83-120">This property is shared by the Informational Flagging Protocol Specification and Task-Related Object Protocol Specification located in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d1b83-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1b83-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d1b83-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d1b83-122">Protocol specifications</span></span>

<span data-ttu-id="d1b83-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1b83-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1b83-124">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d1b83-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d1b83-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1b83-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1b83-126">Especifica las propiedades y operaciones que se permiten en los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="d1b83-126">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d1b83-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d1b83-127">Header files</span></span>

<span data-ttu-id="d1b83-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1b83-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1b83-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d1b83-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1b83-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1b83-130">See also</span></span>



[<span data-ttu-id="d1b83-131">Propiedad can�nico de PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="d1b83-131">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
  
[<span data-ttu-id="d1b83-132">Propiedad can�nico de PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="d1b83-132">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)


[<span data-ttu-id="d1b83-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d1b83-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1b83-134">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d1b83-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1b83-135">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d1b83-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1b83-136">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d1b83-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

