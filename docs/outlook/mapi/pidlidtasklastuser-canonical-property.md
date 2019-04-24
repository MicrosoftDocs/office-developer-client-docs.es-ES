---
title: Propiedad canónica PidLidTaskLastUser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastUser
api_type:
- COM
ms.assetid: 914c55e9-cb36-46a4-b5ee-382413fa25f9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 76311a76001b122bdfd984b9dedc37c2ff878fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360448"
---
# <a name="pidlidtasklastuser-canonical-property"></a><span data-ttu-id="58ca7-103">Propiedad canónica PidLidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="58ca7-103">PidLidTaskLastUser Canonical Property</span></span>

  
  
<span data-ttu-id="58ca7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58ca7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58ca7-105">Nombra el último usuario que era el propietario de la tarea.</span><span class="sxs-lookup"><span data-stu-id="58ca7-105">Names the most recent user who was the task owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="58ca7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="58ca7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="58ca7-107">dispidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="58ca7-107">dispidTaskLastUser</span></span>  <br/> |
|<span data-ttu-id="58ca7-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="58ca7-108">Property set:</span></span>  <br/> |<span data-ttu-id="58ca7-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="58ca7-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="58ca7-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="58ca7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="58ca7-111">0x00008122</span><span class="sxs-lookup"><span data-stu-id="58ca7-111">0x00008122</span></span>  <br/> |
|<span data-ttu-id="58ca7-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="58ca7-112">Data type:</span></span>  <br/> |<span data-ttu-id="58ca7-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="58ca7-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="58ca7-114">Área:</span><span class="sxs-lookup"><span data-stu-id="58ca7-114">Area:</span></span>  <br/> |<span data-ttu-id="58ca7-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="58ca7-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58ca7-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58ca7-116">Remarks</span></span>

<span data-ttu-id="58ca7-117">Antes de que un cliente envíe una solicitud de tarea, establece esta propiedad en el nombre del asignador de tareas.</span><span class="sxs-lookup"><span data-stu-id="58ca7-117">Before a client sends a task request, it sets this property to the name of the task assigner.</span></span> <span data-ttu-id="58ca7-118">Antes de que un cliente envíe una aceptación de tarea, establece esta propiedad en el nombre del usuario al que se asigna la tarea.</span><span class="sxs-lookup"><span data-stu-id="58ca7-118">Before a client sends a task acceptance, it sets this property to the name of the task assignee.</span></span> <span data-ttu-id="58ca7-119">Antes de que un cliente envíe un rechazo de tarea, establece esta propiedad en el nombre del asignador de tareas.</span><span class="sxs-lookup"><span data-stu-id="58ca7-119">Before a client sends a task rejection, it sets this property to the name of the task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="58ca7-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="58ca7-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="58ca7-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="58ca7-121">Protocol specifications</span></span>

<span data-ttu-id="58ca7-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58ca7-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58ca7-123">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="58ca7-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="58ca7-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58ca7-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58ca7-125">Define varios objetos que modelan el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="58ca7-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="58ca7-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="58ca7-126">Header files</span></span>

<span data-ttu-id="58ca7-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="58ca7-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="58ca7-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="58ca7-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58ca7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="58ca7-129">See also</span></span>



[<span data-ttu-id="58ca7-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="58ca7-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="58ca7-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="58ca7-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="58ca7-132">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="58ca7-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="58ca7-133">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="58ca7-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

