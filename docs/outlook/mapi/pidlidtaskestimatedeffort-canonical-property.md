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
ms.openlocfilehash: 5700ab6baaab2a5e73448582a855e6f243d5361d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382802"
---
# <a name="pidlidtaskestimatedeffort-canonical-property"></a><span data-ttu-id="1a170-103">Propiedad canónica PidLidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="1a170-103">PidLidTaskEstimatedEffort Canonical Property</span></span>

  
  
<span data-ttu-id="1a170-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a170-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a170-105">Indica la cantidad de tiempo, en minutos, que se espera que el usuario para realizar una tarea.</span><span class="sxs-lookup"><span data-stu-id="1a170-105">Indicates the amount of time, in minutes, that the user expects to perform a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a170-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1a170-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a170-107">dispidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="1a170-107">dispidTaskEstimatedEffort</span></span>  <br/> |
|<span data-ttu-id="1a170-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="1a170-108">Property set:</span></span>  <br/> |<span data-ttu-id="1a170-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="1a170-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="1a170-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="1a170-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1a170-111">0x00008111</span><span class="sxs-lookup"><span data-stu-id="1a170-111">0x00008111</span></span>  <br/> |
|<span data-ttu-id="1a170-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1a170-112">Data type:</span></span>  <br/> |<span data-ttu-id="1a170-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1a170-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1a170-114">Área:</span><span class="sxs-lookup"><span data-stu-id="1a170-114">Area:</span></span>  <br/> |<span data-ttu-id="1a170-115">Task</span><span class="sxs-lookup"><span data-stu-id="1a170-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a170-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1a170-116">Remarks</span></span>

<span data-ttu-id="1a170-117">El valor debe ser mayor o igual a 0 y menor que 0x5AE980DF (1,525,252,319), donde 480 minutos igual a un día y 2400 minutos igual una semana (ocho horas en un día de trabajo y cinco días en una semana de trabajo).</span><span class="sxs-lookup"><span data-stu-id="1a170-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1a170-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a170-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a170-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1a170-119">Protocol specifications</span></span>

<span data-ttu-id="1a170-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a170-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a170-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1a170-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1a170-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a170-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a170-123">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="1a170-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="1a170-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1a170-124">Header files</span></span>

<span data-ttu-id="1a170-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a170-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a170-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1a170-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a170-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a170-127">See also</span></span>



[<span data-ttu-id="1a170-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1a170-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a170-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1a170-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a170-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1a170-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a170-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="1a170-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

