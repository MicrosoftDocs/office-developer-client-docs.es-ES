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
ms.openlocfilehash: 17f3ac0c5cd6005329212d0dcb458b37bb75f41d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818996"
---
# <a name="pidlidtaskownership-canonical-property"></a><span data-ttu-id="e47c3-103">Propiedad canónica PidLidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="e47c3-103">PidLidTaskOwnership Canonical Property</span></span>

  
  
<span data-ttu-id="e47c3-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e47c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e47c3-105">Indica la función del usuario actual con respecto a la tarea.</span><span class="sxs-lookup"><span data-stu-id="e47c3-105">Indicates the role of the current user relative to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e47c3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e47c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e47c3-107">dispidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="e47c3-107">dispidTaskOwnership</span></span>  <br/> |
|<span data-ttu-id="e47c3-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e47c3-108">Property set:</span></span>  <br/> |<span data-ttu-id="e47c3-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="e47c3-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="e47c3-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="e47c3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e47c3-111">0x00008129</span><span class="sxs-lookup"><span data-stu-id="e47c3-111">0x00008129</span></span>  <br/> |
|<span data-ttu-id="e47c3-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e47c3-112">Data type:</span></span>  <br/> |<span data-ttu-id="e47c3-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e47c3-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e47c3-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e47c3-114">Area:</span></span>  <br/> |<span data-ttu-id="e47c3-115">Task</span><span class="sxs-lookup"><span data-stu-id="e47c3-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e47c3-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e47c3-116">Remarks</span></span>

<span data-ttu-id="e47c3-117">Esta propiedad debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e47c3-117">This property must be one of the following values.</span></span>
  
|<span data-ttu-id="e47c3-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e47c3-118">**Value**</span></span>|<span data-ttu-id="e47c3-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e47c3-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e47c3-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e47c3-120">0x00000000</span></span>  <br/> |<span data-ttu-id="e47c3-121">No se asigna la tarea.</span><span class="sxs-lookup"><span data-stu-id="e47c3-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="e47c3-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e47c3-122">0x00000001</span></span>  <br/> |<span data-ttu-id="e47c3-123">La tarea es copia del asignador de tarea de la tarea.</span><span class="sxs-lookup"><span data-stu-id="e47c3-123">The task is the task assigner's copy of the task.</span></span>  <br/> |
|<span data-ttu-id="e47c3-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e47c3-124">0x00000002</span></span>  <br/> |<span data-ttu-id="e47c3-125">La tarea es copia del encargado de la tarea de la tarea.</span><span class="sxs-lookup"><span data-stu-id="e47c3-125">The task is the task assignee's copy of the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e47c3-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e47c3-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e47c3-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e47c3-127">Protocol specifications</span></span>

<span data-ttu-id="e47c3-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e47c3-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e47c3-129">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e47c3-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e47c3-130">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e47c3-130">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e47c3-131">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="e47c3-131">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e47c3-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e47c3-132">Header files</span></span>

<span data-ttu-id="e47c3-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e47c3-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="e47c3-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e47c3-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e47c3-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="e47c3-135">See also</span></span>



[<span data-ttu-id="e47c3-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e47c3-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e47c3-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e47c3-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e47c3-138">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e47c3-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e47c3-139">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e47c3-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

