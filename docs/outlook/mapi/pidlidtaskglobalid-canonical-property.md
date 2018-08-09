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
ms.openlocfilehash: 33f3b8e7d3d0e0d4461c947aa8e9b3ee66373d2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818957"
---
# <a name="pidlidtaskglobalid-canonical-property"></a><span data-ttu-id="fad99-103">Propiedad canónica PidLidTaskGlobalId</span><span class="sxs-lookup"><span data-stu-id="fad99-103">PidLidTaskGlobalId Canonical Property</span></span>

  
  
<span data-ttu-id="fad99-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fad99-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fad99-105">Busca una tarea existente, mediante el uso de un GUID, tras la recepción de una respuesta de tarea o una actualización de tarea.</span><span class="sxs-lookup"><span data-stu-id="fad99-105">Locates an existing task, by using a GUID, upon receipt of a task response or task update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fad99-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fad99-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fad99-107">dispidTaskGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="fad99-107">dispidTaskGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="fad99-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="fad99-108">Property set:</span></span>  <br/> |<span data-ttu-id="fad99-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="fad99-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="fad99-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="fad99-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fad99-111">0x00008519</span><span class="sxs-lookup"><span data-stu-id="fad99-111">0x00008519</span></span>  <br/> |
|<span data-ttu-id="fad99-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fad99-112">Data type:</span></span>  <br/> |<span data-ttu-id="fad99-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fad99-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fad99-114">Área:</span><span class="sxs-lookup"><span data-stu-id="fad99-114">Area:</span></span>  <br/> |<span data-ttu-id="fad99-115">Task</span><span class="sxs-lookup"><span data-stu-id="fad99-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fad99-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fad99-116">Remarks</span></span>

<span data-ttu-id="fad99-117">Esta propiedad se deja sin establecer para las tareas sin asignar.</span><span class="sxs-lookup"><span data-stu-id="fad99-117">This property is left unset for unassigned tasks.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fad99-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fad99-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fad99-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="fad99-119">Protocol specifications</span></span>

<span data-ttu-id="fad99-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fad99-120">[[MS-OXPROPS] ](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fad99-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fad99-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fad99-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fad99-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fad99-123">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="fad99-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fad99-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fad99-124">Header files</span></span>

<span data-ttu-id="fad99-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fad99-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="fad99-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fad99-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fad99-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="fad99-127">See also</span></span>



[<span data-ttu-id="fad99-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fad99-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fad99-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="fad99-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fad99-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fad99-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fad99-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="fad99-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

