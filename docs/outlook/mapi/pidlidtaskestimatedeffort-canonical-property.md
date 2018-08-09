---
title: Propiedad canónica PidLidTaskEstimatedEffort
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskEstimatedEffort
api_type:
- COM
ms.assetid: c84167d8-f726-45c6-9b21-bcde64473148
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ceb055f6269e7abc8270c7d16da79c041d7f4ed0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818948"
---
# <a name="pidlidtaskestimatedeffort-canonical-property"></a><span data-ttu-id="78989-103">Propiedad canónica PidLidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="78989-103">PidLidTaskEstimatedEffort Canonical Property</span></span>

  
  
<span data-ttu-id="78989-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="78989-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="78989-105">Indica la cantidad de tiempo, en minutos, que se espera que el usuario para realizar una tarea.</span><span class="sxs-lookup"><span data-stu-id="78989-105">Indicates the amount of time, in minutes, that the user expects to perform a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78989-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="78989-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="78989-107">dispidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="78989-107">dispidTaskEstimatedEffort</span></span>  <br/> |
|<span data-ttu-id="78989-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="78989-108">Property set:</span></span>  <br/> |<span data-ttu-id="78989-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="78989-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="78989-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="78989-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="78989-111">0x00008111</span><span class="sxs-lookup"><span data-stu-id="78989-111">0x00008111</span></span>  <br/> |
|<span data-ttu-id="78989-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="78989-112">Data type:</span></span>  <br/> |<span data-ttu-id="78989-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="78989-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="78989-114">Área:</span><span class="sxs-lookup"><span data-stu-id="78989-114">Area:</span></span>  <br/> |<span data-ttu-id="78989-115">Task</span><span class="sxs-lookup"><span data-stu-id="78989-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78989-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="78989-116">Remarks</span></span>

<span data-ttu-id="78989-117">El valor debe ser mayor o igual a 0 y menor que 0x5AE980DF (1,525,252,319), donde 480 minutos igual a un día y 2400 minutos igual una semana (ocho horas en un día de trabajo y cinco días en una semana de trabajo).</span><span class="sxs-lookup"><span data-stu-id="78989-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="78989-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="78989-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="78989-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="78989-119">Protocol specifications</span></span>

<span data-ttu-id="78989-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78989-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78989-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="78989-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="78989-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78989-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78989-123">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="78989-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="78989-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="78989-124">Header files</span></span>

<span data-ttu-id="78989-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="78989-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="78989-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="78989-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="78989-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="78989-127">See also</span></span>



[<span data-ttu-id="78989-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="78989-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="78989-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="78989-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="78989-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="78989-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="78989-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="78989-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

