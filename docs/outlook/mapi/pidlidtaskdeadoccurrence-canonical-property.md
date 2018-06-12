---
title: Propiedad canónico PidLidTaskDeadOccurrence
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDeadOccurrence
api_type:
- COM
ms.assetid: e78287ff-f8cc-45ea-8da8-e7a7359e651c
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 14207e513e935a296ff9b953b92ab1ab9ab41fd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818945"
---
# <a name="pidlidtaskdeadoccurrence-canonical-property"></a><span data-ttu-id="eb384-103">Propiedad canónico PidLidTaskDeadOccurrence</span><span class="sxs-lookup"><span data-stu-id="eb384-103">PidLidTaskDeadOccurrence Canonical Property</span></span>

  
  
<span data-ttu-id="eb384-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb384-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eb384-105">Indica si se deben generar nuevas ocurrencias.</span><span class="sxs-lookup"><span data-stu-id="eb384-105">Indicates whether new occurrences must be generated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb384-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="eb384-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eb384-107">dispidTaskDeadOccur</span><span class="sxs-lookup"><span data-stu-id="eb384-107">dispidTaskDeadOccur</span></span>  <br/> |
|<span data-ttu-id="eb384-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="eb384-108">Property set:</span></span>  <br/> |<span data-ttu-id="eb384-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="eb384-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="eb384-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="eb384-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="eb384-111">0x00008109</span><span class="sxs-lookup"><span data-stu-id="eb384-111">0x00008109</span></span>  <br/> |
|<span data-ttu-id="eb384-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="eb384-112">Data type:</span></span>  <br/> |<span data-ttu-id="eb384-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="eb384-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="eb384-114">Área:</span><span class="sxs-lookup"><span data-stu-id="eb384-114">Area:</span></span>  <br/> |<span data-ttu-id="eb384-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="eb384-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb384-116">Notas</span><span class="sxs-lookup"><span data-stu-id="eb384-116">Remarks</span></span>

<span data-ttu-id="eb384-117">Un patrón de periodicidad ya no está en vigor cuando su última instancia está en el pasado o su número de instancias especificado se ha generado.</span><span class="sxs-lookup"><span data-stu-id="eb384-117">A recurrence pattern is no longer in effect when its final instance is in the past or its specified number of instances has been generated.</span></span> <span data-ttu-id="eb384-118">El cliente establece esta propiedad en FALSE para una nueva tarea o en TRUE cuando genera la última instancia de una tarea periódica.</span><span class="sxs-lookup"><span data-stu-id="eb384-118">The client sets this property to FALSE for a new task or to TRUE when it generates the last instance of a recurring task.</span></span> <span data-ttu-id="eb384-119">Cuando se copia una tarea para generar una nueva instancia, esta propiedad se establece en TRUE en la copia, que es la instancia completada.</span><span class="sxs-lookup"><span data-stu-id="eb384-119">When you copy a task to generate a new instance, this property is set to TRUE on the copy, which is the completed instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eb384-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="eb384-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eb384-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="eb384-121">Protocol specifications</span></span>

<span data-ttu-id="eb384-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb384-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb384-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="eb384-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="eb384-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb384-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb384-125">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="eb384-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="eb384-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="eb384-126">Header files</span></span>

<span data-ttu-id="eb384-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb384-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="eb384-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="eb384-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb384-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="eb384-129">See also</span></span>



[<span data-ttu-id="eb384-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="eb384-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eb384-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="eb384-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eb384-132">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="eb384-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eb384-133">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="eb384-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

