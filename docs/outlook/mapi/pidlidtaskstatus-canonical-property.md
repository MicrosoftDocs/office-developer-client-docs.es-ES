---
title: Propiedad canónico PidLidTaskStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStatus
api_type:
- COM
ms.assetid: 809776b7-ff00-4a52-84b9-8b5fb5f5c3e3
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: e8ca8d7a82360c1f96448b08c9eda18be502b9f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819012"
---
# <a name="pidlidtaskstatus-canonical-property"></a><span data-ttu-id="251bd-103">Propiedad canónico PidLidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="251bd-103">PidLidTaskStatus Canonical Property</span></span>

  
  
<span data-ttu-id="251bd-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="251bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="251bd-105">Especifica el estado de progreso del usuario en la tarea.</span><span class="sxs-lookup"><span data-stu-id="251bd-105">Specifies the status of the user's progress on the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="251bd-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="251bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="251bd-107">dispidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="251bd-107">dispidTaskStatus</span></span>  <br/> |
|<span data-ttu-id="251bd-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="251bd-108">Property set:</span></span>  <br/> |<span data-ttu-id="251bd-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="251bd-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="251bd-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="251bd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="251bd-111">0x00008101</span><span class="sxs-lookup"><span data-stu-id="251bd-111">0x00008101</span></span>  <br/> |
|<span data-ttu-id="251bd-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="251bd-112">Data type:</span></span>  <br/> |<span data-ttu-id="251bd-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="251bd-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="251bd-114">Área:</span><span class="sxs-lookup"><span data-stu-id="251bd-114">Area:</span></span>  <br/> |<span data-ttu-id="251bd-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="251bd-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="251bd-116">Notas</span><span class="sxs-lookup"><span data-stu-id="251bd-116">Remarks</span></span>

<span data-ttu-id="251bd-117">El valor de esta propiedad debe establecerse en uno de estos procedimientos.</span><span class="sxs-lookup"><span data-stu-id="251bd-117">The value of this property must be set to one of the following.</span></span>
  
|<span data-ttu-id="251bd-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="251bd-118">**Value**</span></span>|<span data-ttu-id="251bd-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="251bd-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="251bd-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="251bd-120">0x00000000</span></span>  <br/> |<span data-ttu-id="251bd-121">El usuario no ha iniciado el trabajo en la tarea.</span><span class="sxs-lookup"><span data-stu-id="251bd-121">The user has not started work on the task.</span></span> <span data-ttu-id="251bd-122">Si se establece este valor, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) debe ser 0,0.</span><span class="sxs-lookup"><span data-stu-id="251bd-122">If this value is set, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) must be 0.0.</span></span>  <br/> |
|<span data-ttu-id="251bd-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="251bd-123">0x00000001</span></span>  <br/> |<span data-ttu-id="251bd-124">Trabajo del usuario en esta tarea está en curso.</span><span class="sxs-lookup"><span data-stu-id="251bd-124">The user's work on this task is in progress.</span></span> <span data-ttu-id="251bd-125">Si se establece este valor, **dispidPercentComplete** debe ser mayor que 0,0 y menor que 1,0.</span><span class="sxs-lookup"><span data-stu-id="251bd-125">If this value is set, **dispidPercentComplete** must be greater than 0.0 and less than 1.0.</span></span>  <br/> |
|<span data-ttu-id="251bd-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="251bd-126">0x00000002</span></span>  <br/> |<span data-ttu-id="251bd-127">Trabajo del usuario en esta tarea está completado.</span><span class="sxs-lookup"><span data-stu-id="251bd-127">The user's work on this task is complete.</span></span> <span data-ttu-id="251bd-128">Si se establece este valor, **dispidPercentComplete** debe ser 1.0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) debe ser la fecha actual y **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) debe ser TRUE.</span><span class="sxs-lookup"><span data-stu-id="251bd-128">If this value is set, **dispidPercentComplete** must be 1.0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) must be the current date, and **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) must be TRUE.</span></span>  <br/> |
|<span data-ttu-id="251bd-129">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="251bd-129">0x00000003</span></span>  <br/> |<span data-ttu-id="251bd-130">El usuario está esperando a otra persona.</span><span class="sxs-lookup"><span data-stu-id="251bd-130">The user is waiting on somebody else.</span></span>  <br/> |
|<span data-ttu-id="251bd-131">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="251bd-131">0x00000004</span></span>  <br/> |<span data-ttu-id="251bd-132">El usuario ha diferido el trabajo en la tarea.</span><span class="sxs-lookup"><span data-stu-id="251bd-132">The user has deferred work on the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="251bd-133">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="251bd-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="251bd-134">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="251bd-134">Protocol specifications</span></span>

<span data-ttu-id="251bd-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="251bd-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="251bd-136">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="251bd-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="251bd-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="251bd-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="251bd-138">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="251bd-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="251bd-139">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="251bd-139">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="251bd-140">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="251bd-140">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="251bd-141">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="251bd-141">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="251bd-142">Especifica las propiedades y operaciones para la creación y la ubicación de las carpetas especiales en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="251bd-142">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="251bd-143">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="251bd-143">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="251bd-144">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="251bd-144">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="251bd-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="251bd-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="251bd-146">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="251bd-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="251bd-147">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="251bd-147">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="251bd-148">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="251bd-148">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="251bd-149">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="251bd-149">Header files</span></span>

<span data-ttu-id="251bd-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="251bd-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="251bd-151">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="251bd-151">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="251bd-152">Ver también</span><span class="sxs-lookup"><span data-stu-id="251bd-152">See also</span></span>



[<span data-ttu-id="251bd-153">Propiedad canónico PidLidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="251bd-153">PidLidPercentComplete Canonical Property</span></span>](pidlidpercentcomplete-canonical-property.md)
  
[<span data-ttu-id="251bd-154">Propiedad canónico PidLidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="251bd-154">PidLidTaskDateCompleted Canonical Property</span></span>](pidlidtaskdatecompleted-canonical-property.md)
  
[<span data-ttu-id="251bd-155">Propiedad canónico PidLidTaskComplete</span><span class="sxs-lookup"><span data-stu-id="251bd-155">PidLidTaskComplete Canonical Property</span></span>](pidlidtaskcomplete-canonical-property.md)


[<span data-ttu-id="251bd-156">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="251bd-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="251bd-157">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="251bd-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="251bd-158">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="251bd-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="251bd-159">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="251bd-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

