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
ms.openlocfilehash: cf4edcc22deafe47fccb4fa44782b33aa18b8cec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587183"
---
# <a name="pidlidpercentcomplete-canonical-property"></a><span data-ttu-id="1c0d9-103">Propiedad canónica PidLidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="1c0d9-103">PidLidPercentComplete Canonical Property</span></span>

  
  
<span data-ttu-id="1c0d9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c0d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c0d9-105">Indica que el progreso que el usuario haya realizado en una tarea.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-105">Indicates the progress the user has made on a task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c0d9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1c0d9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1c0d9-107">dispidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="1c0d9-107">dispidPercentComplete</span></span>  <br/> |
|<span data-ttu-id="1c0d9-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="1c0d9-108">Property set:</span></span>  <br/> |<span data-ttu-id="1c0d9-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="1c0d9-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="1c0d9-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="1c0d9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1c0d9-111">0x00008102</span><span class="sxs-lookup"><span data-stu-id="1c0d9-111">0x00008102</span></span>  <br/> |
|<span data-ttu-id="1c0d9-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1c0d9-112">Data type:</span></span>  <br/> |<span data-ttu-id="1c0d9-113">PT_R8</span><span class="sxs-lookup"><span data-stu-id="1c0d9-113">PT_R8</span></span>  <br/> |
|<span data-ttu-id="1c0d9-114">Área:</span><span class="sxs-lookup"><span data-stu-id="1c0d9-114">Area:</span></span>  <br/> |<span data-ttu-id="1c0d9-115">Task</span><span class="sxs-lookup"><span data-stu-id="1c0d9-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c0d9-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1c0d9-116">Remarks</span></span>

<span data-ttu-id="1c0d9-117">El valor de esta propiedad debe ser un número mayor o igual que 0,0 y menor que o igual a 1,0, donde 1.0 indica que el trabajo se ha completado y 0,0 indica que no ha comenzado el trabajo.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-117">The value of this property must be a number greater than or equal to 0.0 and less than or equal to 1.0, where 1.0 indicates that work is completed and 0.0 indicates that work has not begun.</span></span>
  
<span data-ttu-id="1c0d9-118">Para un objeto de mensaje de marca de tiempo, el valor de esta propiedad debe estar establecido a 1,0 si el objeto se marca completado y, en caso contrario, se debe establecer en 0,0.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-118">For a time-flagged message object, the value of this property must be set to 1.0 if the object is flagged completed, and should be set to 0.0 otherwise.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1c0d9-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c0d9-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1c0d9-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1c0d9-120">Protocol specifications</span></span>

<span data-ttu-id="1c0d9-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c0d9-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c0d9-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1c0d9-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c0d9-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c0d9-124">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="1c0d9-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c0d9-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c0d9-126">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-126">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="1c0d9-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c0d9-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c0d9-128">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="1c0d9-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c0d9-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c0d9-130">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="1c0d9-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c0d9-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c0d9-132">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-132">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1c0d9-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1c0d9-133">Header files</span></span>

<span data-ttu-id="1c0d9-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1c0d9-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="1c0d9-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c0d9-136">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1c0d9-136">See also</span></span>



[<span data-ttu-id="1c0d9-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1c0d9-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1c0d9-138">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1c0d9-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1c0d9-139">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1c0d9-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1c0d9-140">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="1c0d9-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

