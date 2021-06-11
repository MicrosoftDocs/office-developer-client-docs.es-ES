---
title: Propiedad canónica PidLidTaskVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskVersion
api_type:
- COM
ms.assetid: 3ab77f25-ad11-4501-8d35-ef560c07e2f2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3daf8a04afc9cf47d808b46f2cee010e15a33cf9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356499"
---
# <a name="pidlidtaskversion-canonical-property"></a><span data-ttu-id="66ec9-103">Propiedad canónica PidLidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="66ec9-103">PidLidTaskVersion Canonical Property</span></span>

  
  
<span data-ttu-id="66ec9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66ec9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66ec9-105">Indica qué copia es la actualización más reciente de una tarea.</span><span class="sxs-lookup"><span data-stu-id="66ec9-105">Indicates which copy is the latest update of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="66ec9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="66ec9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="66ec9-107">dispidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="66ec9-107">dispidTaskVersion</span></span>  <br/> |
|<span data-ttu-id="66ec9-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="66ec9-108">Property set:</span></span>  <br/> |<span data-ttu-id="66ec9-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="66ec9-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="66ec9-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="66ec9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="66ec9-111">0x00008112</span><span class="sxs-lookup"><span data-stu-id="66ec9-111">0x00008112</span></span>  <br/> |
|<span data-ttu-id="66ec9-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="66ec9-112">Data type:</span></span>  <br/> |<span data-ttu-id="66ec9-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="66ec9-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="66ec9-114">Área:</span><span class="sxs-lookup"><span data-stu-id="66ec9-114">Area:</span></span>  <br/> |<span data-ttu-id="66ec9-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="66ec9-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66ec9-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="66ec9-116">Remarks</span></span>

<span data-ttu-id="66ec9-117">Se omiten las actualizaciones con versiones inferiores a la tarea.</span><span class="sxs-lookup"><span data-stu-id="66ec9-117">Updates with lower versions than the task are ignored.</span></span> 
  
<span data-ttu-id="66ec9-118">Al insertar una tarea en una comunicación de tarea, el cliente también establece la versión actual de la tarea incrustada en la comunicación de tarea.</span><span class="sxs-lookup"><span data-stu-id="66ec9-118">When embedding a task in a task communication, the client sets the current version of the embedded task on the task communication as well.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="66ec9-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="66ec9-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="66ec9-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="66ec9-120">Protocol specifications</span></span>

<span data-ttu-id="66ec9-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66ec9-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66ec9-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="66ec9-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="66ec9-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66ec9-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66ec9-124">Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="66ec9-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="66ec9-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="66ec9-125">Header files</span></span>

<span data-ttu-id="66ec9-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66ec9-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="66ec9-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="66ec9-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="66ec9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="66ec9-128">See also</span></span>



[<span data-ttu-id="66ec9-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="66ec9-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="66ec9-130">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="66ec9-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="66ec9-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="66ec9-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="66ec9-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="66ec9-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

