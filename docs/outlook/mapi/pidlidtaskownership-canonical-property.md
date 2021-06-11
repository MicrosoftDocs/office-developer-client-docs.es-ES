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
ms.openlocfilehash: 45fcba3f18aeb9092b71e28a6b68e42ad1abe77d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332112"
---
# <a name="pidlidtaskownership-canonical-property"></a><span data-ttu-id="6d28c-103">Propiedad canónica PidLidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="6d28c-103">PidLidTaskOwnership Canonical Property</span></span>

  
  
<span data-ttu-id="6d28c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d28c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d28c-105">Indica el rol del usuario actual en relación con la tarea.</span><span class="sxs-lookup"><span data-stu-id="6d28c-105">Indicates the role of the current user relative to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6d28c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6d28c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d28c-107">dispidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="6d28c-107">dispidTaskOwnership</span></span>  <br/> |
|<span data-ttu-id="6d28c-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="6d28c-108">Property set:</span></span>  <br/> |<span data-ttu-id="6d28c-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="6d28c-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="6d28c-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="6d28c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6d28c-111">0x00008129</span><span class="sxs-lookup"><span data-stu-id="6d28c-111">0x00008129</span></span>  <br/> |
|<span data-ttu-id="6d28c-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6d28c-112">Data type:</span></span>  <br/> |<span data-ttu-id="6d28c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6d28c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6d28c-114">Área:</span><span class="sxs-lookup"><span data-stu-id="6d28c-114">Area:</span></span>  <br/> |<span data-ttu-id="6d28c-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="6d28c-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d28c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6d28c-116">Remarks</span></span>

<span data-ttu-id="6d28c-117">Esta propiedad debe ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="6d28c-117">This property must be one of the following values.</span></span>
  
|<span data-ttu-id="6d28c-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6d28c-118">**Value**</span></span>|<span data-ttu-id="6d28c-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6d28c-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6d28c-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6d28c-120">0x00000000</span></span>  <br/> |<span data-ttu-id="6d28c-121">La tarea no está asignada.</span><span class="sxs-lookup"><span data-stu-id="6d28c-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="6d28c-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6d28c-122">0x00000001</span></span>  <br/> |<span data-ttu-id="6d28c-123">La tarea es la copia del asignador de tareas de la tarea.</span><span class="sxs-lookup"><span data-stu-id="6d28c-123">The task is the task assigner's copy of the task.</span></span>  <br/> |
|<span data-ttu-id="6d28c-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6d28c-124">0x00000002</span></span>  <br/> |<span data-ttu-id="6d28c-125">La tarea es la copia del usuario asignado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="6d28c-125">The task is the task assignee's copy of the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="6d28c-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6d28c-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6d28c-127">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="6d28c-127">Protocol specifications</span></span>

<span data-ttu-id="6d28c-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d28c-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d28c-129">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="6d28c-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6d28c-130">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d28c-130">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d28c-131">Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="6d28c-131">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6d28c-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6d28c-132">Header files</span></span>

<span data-ttu-id="6d28c-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6d28c-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d28c-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6d28c-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d28c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d28c-135">See also</span></span>



[<span data-ttu-id="6d28c-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6d28c-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d28c-137">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="6d28c-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d28c-138">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6d28c-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d28c-139">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="6d28c-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

