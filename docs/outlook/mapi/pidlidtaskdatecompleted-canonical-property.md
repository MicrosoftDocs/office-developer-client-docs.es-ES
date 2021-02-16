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
ms.openlocfilehash: 3096e7ab2133d2984be0534cb091d61d2c7157bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303216"
---
# <a name="pidlidtaskdatecompleted-canonical-property"></a><span data-ttu-id="74134-103">Propiedad canónica PidLidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="74134-103">PidLidTaskDateCompleted Canonical Property</span></span>

  
  
<span data-ttu-id="74134-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74134-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74134-105">Especifica la fecha en que el usuario completa la tarea.</span><span class="sxs-lookup"><span data-stu-id="74134-105">Specifies the date when the user completes the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74134-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="74134-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74134-107">dispidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="74134-107">dispidTaskDateCompleted</span></span>  <br/> |
|<span data-ttu-id="74134-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="74134-108">Property set:</span></span>  <br/> |<span data-ttu-id="74134-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="74134-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="74134-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="74134-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="74134-111">0x0000810F</span><span class="sxs-lookup"><span data-stu-id="74134-111">0x0000810F</span></span>  <br/> |
|<span data-ttu-id="74134-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="74134-112">Data type:</span></span>  <br/> |<span data-ttu-id="74134-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="74134-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="74134-114">Área:</span><span class="sxs-lookup"><span data-stu-id="74134-114">Area:</span></span>  <br/> |<span data-ttu-id="74134-115">Task</span><span class="sxs-lookup"><span data-stu-id="74134-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74134-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74134-116">Remarks</span></span>

<span data-ttu-id="74134-117">Si se establece, esta propiedad debe tener un componente de hora de medianoche en la zona horaria local, convertido a hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="74134-117">If set, this property must have a time component of midnight in the local time zone, converted to Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="74134-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="74134-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="74134-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="74134-119">Protocol specifications</span></span>

<span data-ttu-id="74134-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74134-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74134-121">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="74134-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="74134-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74134-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74134-123">Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="74134-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="74134-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="74134-124">Header files</span></span>

<span data-ttu-id="74134-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74134-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="74134-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="74134-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74134-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="74134-127">See also</span></span>



[<span data-ttu-id="74134-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="74134-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74134-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="74134-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74134-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="74134-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74134-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="74134-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

