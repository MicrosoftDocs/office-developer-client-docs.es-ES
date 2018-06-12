---
title: Propiedad canónico PidLidTaskMultipleRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMultipleRecipients
api_type:
- COM
ms.assetid: 28ba9997-72dd-465f-94a7-35a317a361ef
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 1e1cba3d927072cb03dbd34eee518c9b0a9e0383
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818978"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a><span data-ttu-id="f462d-103">Propiedad canónico PidLidTaskMultipleRecipients</span><span class="sxs-lookup"><span data-stu-id="f462d-103">PidLidTaskMultipleRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="f462d-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f462d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f462d-105">Proporciona optimización de las sugerencias acerca de los destinatarios de una tarea.</span><span class="sxs-lookup"><span data-stu-id="f462d-105">Provides optimization hints about the recipients of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f462d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f462d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f462d-107">dispidTaskMultRecips</span><span class="sxs-lookup"><span data-stu-id="f462d-107">dispidTaskMultRecips</span></span>  <br/> |
|<span data-ttu-id="f462d-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="f462d-108">Property set:</span></span>  <br/> |<span data-ttu-id="f462d-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="f462d-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="f462d-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="f462d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f462d-111">0x00008120</span><span class="sxs-lookup"><span data-stu-id="f462d-111">0x00008120</span></span>  <br/> |
|<span data-ttu-id="f462d-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f462d-112">Data type:</span></span>  <br/> |<span data-ttu-id="f462d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f462d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f462d-114">Área:</span><span class="sxs-lookup"><span data-stu-id="f462d-114">Area:</span></span>  <br/> |<span data-ttu-id="f462d-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="f462d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f462d-116">Notas</span><span class="sxs-lookup"><span data-stu-id="f462d-116">Remarks</span></span>

<span data-ttu-id="f462d-117">Si se establece, esta propiedad debe establecerse en una operación **OR** bit a bit de cero o más de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="f462d-117">If set, this property must be set to a bitwise **OR** operation of zero or more of the following values.</span></span> 
  
|<span data-ttu-id="f462d-118">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="f462d-118">**Name**</span></span>|<span data-ttu-id="f462d-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f462d-119">**Value**</span></span>|<span data-ttu-id="f462d-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f462d-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f462d-121">Enviado</span><span class="sxs-lookup"><span data-stu-id="f462d-121">Sent</span></span>  <br/> |<span data-ttu-id="f462d-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f462d-122">0x00000001</span></span>  <br/> |<span data-ttu-id="f462d-123">La tarea tiene varios destinatarios principales.</span><span class="sxs-lookup"><span data-stu-id="f462d-123">The task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="f462d-124">Cantidad.Recibida</span><span class="sxs-lookup"><span data-stu-id="f462d-124">Received</span></span>  <br/> |<span data-ttu-id="f462d-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f462d-125">0x00000002</span></span>  <br/> |<span data-ttu-id="f462d-126">Aunque la sugerencia enviados no estuviera presente, el cliente detecta que la tarea tiene varios destinatarios principales.</span><span class="sxs-lookup"><span data-stu-id="f462d-126">Although the Sent hint was not present, the client detected that the task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="f462d-127">Reservado</span><span class="sxs-lookup"><span data-stu-id="f462d-127">Reserved</span></span>  <br/> |<span data-ttu-id="f462d-128">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="f462d-128">0x00000004</span></span>  <br/> |<span data-ttu-id="f462d-129">Este valor está reservado.</span><span class="sxs-lookup"><span data-stu-id="f462d-129">This value is reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f462d-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f462d-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f462d-131">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f462d-131">Protocol specifications</span></span>

<span data-ttu-id="f462d-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f462d-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f462d-133">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f462d-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f462d-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f462d-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f462d-135">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="f462d-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f462d-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f462d-136">Header files</span></span>

<span data-ttu-id="f462d-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f462d-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="f462d-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f462d-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f462d-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="f462d-139">See also</span></span>



[<span data-ttu-id="f462d-140">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f462d-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f462d-141">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f462d-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f462d-142">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="f462d-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f462d-143">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f462d-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

