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
ms.openlocfilehash: 295eb9dcc6da7b0fb6c6fd7ea0b73134ffaadb3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303020"
---
# <a name="pidlidtaskglobalid-canonical-property"></a><span data-ttu-id="fefba-103">Propiedad canónica PidLidTaskGlobalId</span><span class="sxs-lookup"><span data-stu-id="fefba-103">PidLidTaskGlobalId Canonical Property</span></span>

  
  
<span data-ttu-id="fefba-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fefba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fefba-105">Localiza una tarea existente, mediante un GUID, al recibir una respuesta de tarea o una actualización de tarea.</span><span class="sxs-lookup"><span data-stu-id="fefba-105">Locates an existing task, by using a GUID, upon receipt of a task response or task update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fefba-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fefba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fefba-107">dispidTaskGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="fefba-107">dispidTaskGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="fefba-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="fefba-108">Property set:</span></span>  <br/> |<span data-ttu-id="fefba-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="fefba-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="fefba-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="fefba-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fefba-111">0x00008519</span><span class="sxs-lookup"><span data-stu-id="fefba-111">0x00008519</span></span>  <br/> |
|<span data-ttu-id="fefba-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fefba-112">Data type:</span></span>  <br/> |<span data-ttu-id="fefba-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fefba-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fefba-114">Área:</span><span class="sxs-lookup"><span data-stu-id="fefba-114">Area:</span></span>  <br/> |<span data-ttu-id="fefba-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="fefba-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fefba-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fefba-116">Remarks</span></span>

<span data-ttu-id="fefba-117">Esta propiedad se deja sin conjunto para las tareas sin signo.</span><span class="sxs-lookup"><span data-stu-id="fefba-117">This property is left unset for unassigned tasks.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fefba-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fefba-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fefba-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="fefba-119">Protocol specifications</span></span>

<span data-ttu-id="fefba-120">[[MS-OXPROPS] ](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fefba-120">[[MS-OXPROPS] ](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fefba-121">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="fefba-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fefba-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fefba-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fefba-123">Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="fefba-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fefba-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fefba-124">Header files</span></span>

<span data-ttu-id="fefba-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fefba-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="fefba-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fefba-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fefba-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="fefba-127">See also</span></span>



[<span data-ttu-id="fefba-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fefba-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fefba-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fefba-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fefba-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fefba-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fefba-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="fefba-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

