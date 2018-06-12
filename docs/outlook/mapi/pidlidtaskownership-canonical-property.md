---
title: Propiedad canónico PidLidTaskOwnership
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 17f3ac0c5cd6005329212d0dcb458b37bb75f41d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818996"
---
# <a name="pidlidtaskownership-canonical-property"></a><span data-ttu-id="79274-103">Propiedad canónico PidLidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="79274-103">PidLidTaskOwnership Canonical Property</span></span>

  
  
<span data-ttu-id="79274-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="79274-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="79274-105">Indica la función del usuario actual con respecto a la tarea.</span><span class="sxs-lookup"><span data-stu-id="79274-105">Indicates the role of the current user relative to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="79274-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="79274-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="79274-107">dispidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="79274-107">dispidTaskOwnership</span></span>  <br/> |
|<span data-ttu-id="79274-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="79274-108">Property set:</span></span>  <br/> |<span data-ttu-id="79274-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="79274-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="79274-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="79274-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="79274-111">0x00008129</span><span class="sxs-lookup"><span data-stu-id="79274-111">0x00008129</span></span>  <br/> |
|<span data-ttu-id="79274-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="79274-112">Data type:</span></span>  <br/> |<span data-ttu-id="79274-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="79274-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="79274-114">Área:</span><span class="sxs-lookup"><span data-stu-id="79274-114">Area:</span></span>  <br/> |<span data-ttu-id="79274-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="79274-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79274-116">Notas</span><span class="sxs-lookup"><span data-stu-id="79274-116">Remarks</span></span>

<span data-ttu-id="79274-117">Esta propiedad debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="79274-117">This property must be one of the following values.</span></span>
  
|<span data-ttu-id="79274-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="79274-118">**Value**</span></span>|<span data-ttu-id="79274-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="79274-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="79274-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79274-120">0x00000000</span></span>  <br/> |<span data-ttu-id="79274-121">No se asigna la tarea.</span><span class="sxs-lookup"><span data-stu-id="79274-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="79274-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="79274-122">0x00000001</span></span>  <br/> |<span data-ttu-id="79274-123">La tarea es copia del asignador de tarea de la tarea.</span><span class="sxs-lookup"><span data-stu-id="79274-123">The task is the task assigner's copy of the task.</span></span>  <br/> |
|<span data-ttu-id="79274-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="79274-124">0x00000002</span></span>  <br/> |<span data-ttu-id="79274-125">La tarea es copia del encargado de la tarea de la tarea.</span><span class="sxs-lookup"><span data-stu-id="79274-125">The task is the task assignee's copy of the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="79274-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="79274-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="79274-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="79274-127">Protocol specifications</span></span>

<span data-ttu-id="79274-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79274-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79274-129">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="79274-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="79274-130">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79274-130">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79274-131">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="79274-131">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="79274-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="79274-132">Header files</span></span>

<span data-ttu-id="79274-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="79274-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="79274-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="79274-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="79274-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="79274-135">See also</span></span>



[<span data-ttu-id="79274-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="79274-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="79274-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="79274-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="79274-138">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="79274-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="79274-139">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="79274-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

