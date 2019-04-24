---
title: Propiedad canónica PidLidPercentComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidPercentComplete
api_type:
- COM
ms.assetid: e63792b1-9580-4702-a6d7-dd3ae5007a4a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 870b4e0edb360ac36525f94b0605af930eee8fa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357977"
---
# <a name="pidlidpercentcomplete-canonical-property"></a><span data-ttu-id="9d1e9-103">Propiedad canónica PidLidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="9d1e9-103">PidLidPercentComplete Canonical Property</span></span>

  
  
<span data-ttu-id="9d1e9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d1e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d1e9-105">Indica el progreso realizado por el usuario en una tarea.</span><span class="sxs-lookup"><span data-stu-id="9d1e9-105">Indicates the progress the user has made on a task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d1e9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9d1e9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d1e9-107">dispidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="9d1e9-107">dispidPercentComplete</span></span>  <br/> |
|<span data-ttu-id="9d1e9-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="9d1e9-108">Property set:</span></span>  <br/> |<span data-ttu-id="9d1e9-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="9d1e9-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="9d1e9-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="9d1e9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9d1e9-111">0x00008102</span><span class="sxs-lookup"><span data-stu-id="9d1e9-111">0x00008102</span></span>  <br/> |
|<span data-ttu-id="9d1e9-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9d1e9-112">Data type:</span></span>  <br/> |<span data-ttu-id="9d1e9-113">PT_R8</span><span class="sxs-lookup"><span data-stu-id="9d1e9-113">PT_R8</span></span>  <br/> |
|<span data-ttu-id="9d1e9-114">Área:</span><span class="sxs-lookup"><span data-stu-id="9d1e9-114">Area:</span></span>  <br/> |<span data-ttu-id="9d1e9-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="9d1e9-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d1e9-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9d1e9-116">Remarks</span></span>

<span data-ttu-id="9d1e9-117">El valor de esta propiedad debe ser un número mayor o igual que 0,0 y menor o igual que 1,0, donde 1,0 indica que se ha completado el trabajo y 0,0 indica que el trabajo no ha empezado.</span><span class="sxs-lookup"><span data-stu-id="9d1e9-117">The value of this property must be a number greater than or equal to 0.0 and less than or equal to 1.0, where 1.0 indicates that work is completed and 0.0 indicates that work has not begun.</span></span>
  
<span data-ttu-id="9d1e9-118">Para un objeto de mensaje con marca de tiempo, el valor de esta propiedad debe establecerse en 1,0 si el objeto está marcado como completado y debe establecerse en 0,0 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9d1e9-118">For a time-flagged message object, the value of this property must be set to 1.0 if the object is flagged completed, and should be set to 0.0 otherwise.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9d1e9-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9d1e9-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9d1e9-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="9d1e9-120">Protocol specifications</span></span>

<span data-ttu-id="9d1e9-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d1e9-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d1e9-122">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9d1e9-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9d1e9-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d1e9-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d1e9-124">Define varios objetos que modelan el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="9d1e9-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="9d1e9-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d1e9-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d1e9-126">Especifica las propiedades y operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="9d1e9-126">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="9d1e9-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d1e9-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d1e9-128">Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="9d1e9-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="9d1e9-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d1e9-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d1e9-130">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="9d1e9-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="9d1e9-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d1e9-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d1e9-132">Controla el orden y el flujo de transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="9d1e9-132">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9d1e9-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9d1e9-133">Header files</span></span>

<span data-ttu-id="9d1e9-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9d1e9-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d1e9-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9d1e9-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d1e9-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d1e9-136">See also</span></span>



[<span data-ttu-id="9d1e9-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9d1e9-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d1e9-138">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="9d1e9-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d1e9-139">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9d1e9-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d1e9-140">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="9d1e9-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

