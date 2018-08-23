---
title: Propiedad canónica PidLidTaskDateCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDateCompleted
api_type:
- COM
ms.assetid: ae384529-55e2-4da1-9a41-acc292591a7c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 97d541279f052099498cdf7bfd374a95238a376d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584222"
---
# <a name="pidlidtaskdatecompleted-canonical-property"></a><span data-ttu-id="4282e-103">Propiedad canónica PidLidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="4282e-103">PidLidTaskDateCompleted Canonical Property</span></span>

  
  
<span data-ttu-id="4282e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4282e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4282e-105">Especifica la fecha cuando el usuario complete la tarea.</span><span class="sxs-lookup"><span data-stu-id="4282e-105">Specifies the date when the user completes the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4282e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4282e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4282e-107">dispidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="4282e-107">dispidTaskDateCompleted</span></span>  <br/> |
|<span data-ttu-id="4282e-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="4282e-108">Property set:</span></span>  <br/> |<span data-ttu-id="4282e-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="4282e-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="4282e-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="4282e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4282e-111">0x0000810F</span><span class="sxs-lookup"><span data-stu-id="4282e-111">0x0000810F</span></span>  <br/> |
|<span data-ttu-id="4282e-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4282e-112">Data type:</span></span>  <br/> |<span data-ttu-id="4282e-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="4282e-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="4282e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="4282e-114">Area:</span></span>  <br/> |<span data-ttu-id="4282e-115">Task</span><span class="sxs-lookup"><span data-stu-id="4282e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4282e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4282e-116">Remarks</span></span>

<span data-ttu-id="4282e-117">Si se establece, esta propiedad debe tener un componente de hora de la medianoche en la zona horaria local, convertir a hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="4282e-117">If set, this property must have a time component of midnight in the local time zone, converted to Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4282e-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4282e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4282e-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="4282e-119">Protocol specifications</span></span>

<span data-ttu-id="4282e-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4282e-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4282e-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4282e-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4282e-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4282e-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4282e-123">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="4282e-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="4282e-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4282e-124">Header files</span></span>

<span data-ttu-id="4282e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4282e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4282e-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4282e-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4282e-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="4282e-127">See also</span></span>



[<span data-ttu-id="4282e-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4282e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4282e-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4282e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4282e-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4282e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4282e-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="4282e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

