---
title: Propiedad canónica PidLidTaskGlobalId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskGlobalId
api_type:
- COM
ms.assetid: 369d8c78-3cf6-4a55-ba14-9da0377d6ccf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4f91b4cdeb301eba6eb9753fc5e7dc3e3d5d892c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592622"
---
# <a name="pidlidtaskglobalid-canonical-property"></a><span data-ttu-id="64244-103">Propiedad canónica PidLidTaskGlobalId</span><span class="sxs-lookup"><span data-stu-id="64244-103">PidLidTaskGlobalId Canonical Property</span></span>

  
  
<span data-ttu-id="64244-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64244-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64244-105">Busca una tarea existente, mediante el uso de un GUID, tras la recepción de una respuesta de tarea o una actualización de tarea.</span><span class="sxs-lookup"><span data-stu-id="64244-105">Locates an existing task, by using a GUID, upon receipt of a task response or task update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64244-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="64244-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64244-107">dispidTaskGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="64244-107">dispidTaskGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="64244-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="64244-108">Property set:</span></span>  <br/> |<span data-ttu-id="64244-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="64244-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="64244-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="64244-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="64244-111">0x00008519</span><span class="sxs-lookup"><span data-stu-id="64244-111">0x00008519</span></span>  <br/> |
|<span data-ttu-id="64244-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="64244-112">Data type:</span></span>  <br/> |<span data-ttu-id="64244-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="64244-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="64244-114">Área:</span><span class="sxs-lookup"><span data-stu-id="64244-114">Area:</span></span>  <br/> |<span data-ttu-id="64244-115">Task</span><span class="sxs-lookup"><span data-stu-id="64244-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64244-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="64244-116">Remarks</span></span>

<span data-ttu-id="64244-117">Esta propiedad se deja sin establecer para las tareas sin asignar.</span><span class="sxs-lookup"><span data-stu-id="64244-117">This property is left unset for unassigned tasks.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="64244-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="64244-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="64244-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="64244-119">Protocol specifications</span></span>

<span data-ttu-id="64244-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64244-120">[[MS-OXPROPS] ](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64244-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="64244-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="64244-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64244-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64244-123">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="64244-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="64244-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="64244-124">Header files</span></span>

<span data-ttu-id="64244-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64244-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="64244-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="64244-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64244-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="64244-127">See also</span></span>



[<span data-ttu-id="64244-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="64244-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64244-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="64244-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64244-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="64244-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64244-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="64244-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

