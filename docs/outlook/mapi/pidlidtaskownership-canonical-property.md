---
title: Propiedad canónica PidLidTaskOwnership
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOwnership
api_type:
- COM
ms.assetid: 805dcb6c-f405-4c4d-8bca-af4bd9cd44fa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5c335d8fab820c9876adbe8f001696a02068460c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591411"
---
# <a name="pidlidtaskownership-canonical-property"></a><span data-ttu-id="5c9a9-103">Propiedad canónica PidLidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="5c9a9-103">PidLidTaskOwnership Canonical Property</span></span>

  
  
<span data-ttu-id="5c9a9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c9a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c9a9-105">Indica la función del usuario actual con respecto a la tarea.</span><span class="sxs-lookup"><span data-stu-id="5c9a9-105">Indicates the role of the current user relative to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5c9a9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5c9a9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c9a9-107">dispidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="5c9a9-107">dispidTaskOwnership</span></span>  <br/> |
|<span data-ttu-id="5c9a9-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="5c9a9-108">Property set:</span></span>  <br/> |<span data-ttu-id="5c9a9-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="5c9a9-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="5c9a9-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="5c9a9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5c9a9-111">0x00008129</span><span class="sxs-lookup"><span data-stu-id="5c9a9-111">0x00008129</span></span>  <br/> |
|<span data-ttu-id="5c9a9-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5c9a9-112">Data type:</span></span>  <br/> |<span data-ttu-id="5c9a9-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5c9a9-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5c9a9-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5c9a9-114">Area:</span></span>  <br/> |<span data-ttu-id="5c9a9-115">Task</span><span class="sxs-lookup"><span data-stu-id="5c9a9-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c9a9-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5c9a9-116">Remarks</span></span>

<span data-ttu-id="5c9a9-117">Esta propiedad debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5c9a9-117">This property must be one of the following values.</span></span>
  
|<span data-ttu-id="5c9a9-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5c9a9-118">**Value**</span></span>|<span data-ttu-id="5c9a9-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5c9a9-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c9a9-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c9a9-120">0x00000000</span></span>  <br/> |<span data-ttu-id="5c9a9-121">No se asigna la tarea.</span><span class="sxs-lookup"><span data-stu-id="5c9a9-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="5c9a9-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5c9a9-122">0x00000001</span></span>  <br/> |<span data-ttu-id="5c9a9-123">La tarea es copia del asignador de tarea de la tarea.</span><span class="sxs-lookup"><span data-stu-id="5c9a9-123">The task is the task assigner's copy of the task.</span></span>  <br/> |
|<span data-ttu-id="5c9a9-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5c9a9-124">0x00000002</span></span>  <br/> |<span data-ttu-id="5c9a9-125">La tarea es copia del encargado de la tarea de la tarea.</span><span class="sxs-lookup"><span data-stu-id="5c9a9-125">The task is the task assignee's copy of the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5c9a9-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c9a9-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5c9a9-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5c9a9-127">Protocol specifications</span></span>

<span data-ttu-id="5c9a9-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c9a9-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c9a9-129">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5c9a9-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5c9a9-130">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c9a9-130">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c9a9-131">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="5c9a9-131">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5c9a9-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5c9a9-132">Header files</span></span>

<span data-ttu-id="5c9a9-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c9a9-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c9a9-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5c9a9-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c9a9-135">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5c9a9-135">See also</span></span>



[<span data-ttu-id="5c9a9-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5c9a9-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5c9a9-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5c9a9-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5c9a9-138">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5c9a9-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5c9a9-139">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5c9a9-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

