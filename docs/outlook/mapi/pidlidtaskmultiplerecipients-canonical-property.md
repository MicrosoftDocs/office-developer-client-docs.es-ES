---
title: Propiedad canónica PidLidTaskMultipleRecipients
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f20c3e988c0a0461a966a109a8d345c22e1fccee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585741"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a><span data-ttu-id="ac87e-103">Propiedad canónica PidLidTaskMultipleRecipients</span><span class="sxs-lookup"><span data-stu-id="ac87e-103">PidLidTaskMultipleRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="ac87e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac87e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac87e-105">Proporciona optimización de las sugerencias acerca de los destinatarios de una tarea.</span><span class="sxs-lookup"><span data-stu-id="ac87e-105">Provides optimization hints about the recipients of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac87e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ac87e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac87e-107">dispidTaskMultRecips</span><span class="sxs-lookup"><span data-stu-id="ac87e-107">dispidTaskMultRecips</span></span>  <br/> |
|<span data-ttu-id="ac87e-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="ac87e-108">Property set:</span></span>  <br/> |<span data-ttu-id="ac87e-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="ac87e-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="ac87e-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="ac87e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ac87e-111">0x00008120</span><span class="sxs-lookup"><span data-stu-id="ac87e-111">0x00008120</span></span>  <br/> |
|<span data-ttu-id="ac87e-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ac87e-112">Data type:</span></span>  <br/> |<span data-ttu-id="ac87e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ac87e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ac87e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ac87e-114">Area:</span></span>  <br/> |<span data-ttu-id="ac87e-115">Task</span><span class="sxs-lookup"><span data-stu-id="ac87e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac87e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ac87e-116">Remarks</span></span>

<span data-ttu-id="ac87e-117">Si se establece, esta propiedad debe establecerse en una operación **OR** bit a bit de cero o más de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="ac87e-117">If set, this property must be set to a bitwise **OR** operation of zero or more of the following values.</span></span> 
  
|<span data-ttu-id="ac87e-118">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="ac87e-118">**Name**</span></span>|<span data-ttu-id="ac87e-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ac87e-119">**Value**</span></span>|<span data-ttu-id="ac87e-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ac87e-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac87e-121">Enviado</span><span class="sxs-lookup"><span data-stu-id="ac87e-121">Sent</span></span>  <br/> |<span data-ttu-id="ac87e-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ac87e-122">0x00000001</span></span>  <br/> |<span data-ttu-id="ac87e-123">La tarea tiene varios destinatarios principales.</span><span class="sxs-lookup"><span data-stu-id="ac87e-123">The task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="ac87e-124">Cantidad.Recibida</span><span class="sxs-lookup"><span data-stu-id="ac87e-124">Received</span></span>  <br/> |<span data-ttu-id="ac87e-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ac87e-125">0x00000002</span></span>  <br/> |<span data-ttu-id="ac87e-126">Aunque la sugerencia enviados no estuviera presente, el cliente detecta que la tarea tiene varios destinatarios principales.</span><span class="sxs-lookup"><span data-stu-id="ac87e-126">Although the Sent hint was not present, the client detected that the task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="ac87e-127">Reservado</span><span class="sxs-lookup"><span data-stu-id="ac87e-127">Reserved</span></span>  <br/> |<span data-ttu-id="ac87e-128">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="ac87e-128">0x00000004</span></span>  <br/> |<span data-ttu-id="ac87e-129">Este valor está reservado.</span><span class="sxs-lookup"><span data-stu-id="ac87e-129">This value is reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ac87e-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac87e-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ac87e-131">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="ac87e-131">Protocol specifications</span></span>

<span data-ttu-id="ac87e-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac87e-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac87e-133">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ac87e-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ac87e-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac87e-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac87e-135">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="ac87e-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ac87e-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ac87e-136">Header files</span></span>

<span data-ttu-id="ac87e-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac87e-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac87e-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ac87e-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac87e-139">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ac87e-139">See also</span></span>



[<span data-ttu-id="ac87e-140">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ac87e-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac87e-141">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="ac87e-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac87e-142">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ac87e-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac87e-143">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="ac87e-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

