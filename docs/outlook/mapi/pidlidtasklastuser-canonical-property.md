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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390936"
---
# <a name="pidlidtasklastuser-canonical-property"></a><span data-ttu-id="a1c8a-103">Propiedad canónica PidLidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="a1c8a-103">PidLidTaskLastUser Canonical Property</span></span>

  
  
<span data-ttu-id="a1c8a-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1c8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1c8a-105">Nombres de usuario más reciente que era el propietario de la tarea.</span><span class="sxs-lookup"><span data-stu-id="a1c8a-105">Names the most recent user who was the task owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1c8a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a1c8a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1c8a-107">dispidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="a1c8a-107">dispidTaskLastUser</span></span>  <br/> |
|<span data-ttu-id="a1c8a-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="a1c8a-108">Property set:</span></span>  <br/> |<span data-ttu-id="a1c8a-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="a1c8a-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="a1c8a-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="a1c8a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a1c8a-111">0x00008122</span><span class="sxs-lookup"><span data-stu-id="a1c8a-111">0x00008122</span></span>  <br/> |
|<span data-ttu-id="a1c8a-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a1c8a-112">Data type:</span></span>  <br/> |<span data-ttu-id="a1c8a-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a1c8a-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a1c8a-114">Área:</span><span class="sxs-lookup"><span data-stu-id="a1c8a-114">Area:</span></span>  <br/> |<span data-ttu-id="a1c8a-115">Task</span><span class="sxs-lookup"><span data-stu-id="a1c8a-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1c8a-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a1c8a-116">Remarks</span></span>

<span data-ttu-id="a1c8a-117">Antes de que un cliente envía una solicitud de tarea, se establece esta propiedad en el nombre de asignador de la tarea.</span><span class="sxs-lookup"><span data-stu-id="a1c8a-117">Before a client sends a task request, it sets this property to the name of the task assigner.</span></span> <span data-ttu-id="a1c8a-118">Antes de que un cliente envía una aceptación de la tarea, se establece esta propiedad en el nombre de usuario asignado a la tarea.</span><span class="sxs-lookup"><span data-stu-id="a1c8a-118">Before a client sends a task acceptance, it sets this property to the name of the task assignee.</span></span> <span data-ttu-id="a1c8a-119">Antes de que un cliente envía un rechazo de tarea, establece esta propiedad en el nombre de asignador de la tarea.</span><span class="sxs-lookup"><span data-stu-id="a1c8a-119">Before a client sends a task rejection, it sets this property to the name of the task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a1c8a-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1c8a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a1c8a-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a1c8a-121">Protocol specifications</span></span>

<span data-ttu-id="a1c8a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1c8a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1c8a-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a1c8a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a1c8a-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1c8a-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1c8a-125">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="a1c8a-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a1c8a-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a1c8a-126">Header files</span></span>

<span data-ttu-id="a1c8a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1c8a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1c8a-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a1c8a-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1c8a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1c8a-129">See also</span></span>



[<span data-ttu-id="a1c8a-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a1c8a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1c8a-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a1c8a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1c8a-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a1c8a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1c8a-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="a1c8a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

