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
ms.openlocfilehash: 3b260917e107086dee6176f73b6c82c3a1825327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360070"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a><span data-ttu-id="45cac-103">Propiedad canónica PidLidTaskMultipleRecipients</span><span class="sxs-lookup"><span data-stu-id="45cac-103">PidLidTaskMultipleRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="45cac-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45cac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45cac-105">Proporciona sugerencias de optimización sobre los destinatarios de una tarea.</span><span class="sxs-lookup"><span data-stu-id="45cac-105">Provides optimization hints about the recipients of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45cac-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="45cac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45cac-107">dispidTaskMultRecips</span><span class="sxs-lookup"><span data-stu-id="45cac-107">dispidTaskMultRecips</span></span>  <br/> |
|<span data-ttu-id="45cac-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="45cac-108">Property set:</span></span>  <br/> |<span data-ttu-id="45cac-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="45cac-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="45cac-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="45cac-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="45cac-111">0x00008120</span><span class="sxs-lookup"><span data-stu-id="45cac-111">0x00008120</span></span>  <br/> |
|<span data-ttu-id="45cac-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="45cac-112">Data type:</span></span>  <br/> |<span data-ttu-id="45cac-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="45cac-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="45cac-114">Área:</span><span class="sxs-lookup"><span data-stu-id="45cac-114">Area:</span></span>  <br/> |<span data-ttu-id="45cac-115">Task</span><span class="sxs-lookup"><span data-stu-id="45cac-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45cac-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="45cac-116">Remarks</span></span>

<span data-ttu-id="45cac-117">Si se establece, esta propiedad debe establecerse en una operación **OR** bit a bit de cero o más de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="45cac-117">If set, this property must be set to a bitwise **OR** operation of zero or more of the following values.</span></span> 
  
|<span data-ttu-id="45cac-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="45cac-118">**Name**</span></span>|<span data-ttu-id="45cac-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="45cac-119">**Value**</span></span>|<span data-ttu-id="45cac-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="45cac-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="45cac-121">Sent</span><span class="sxs-lookup"><span data-stu-id="45cac-121">Sent</span></span>  <br/> |<span data-ttu-id="45cac-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="45cac-122">0x00000001</span></span>  <br/> |<span data-ttu-id="45cac-123">La tarea tiene varios destinatarios principales.</span><span class="sxs-lookup"><span data-stu-id="45cac-123">The task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="45cac-124">Cantidad.Recibida</span><span class="sxs-lookup"><span data-stu-id="45cac-124">Received</span></span>  <br/> |<span data-ttu-id="45cac-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="45cac-125">0x00000002</span></span>  <br/> |<span data-ttu-id="45cac-126">Aunque la sugerencia enviada no estaba presente, el cliente detectó que la tarea tiene varios destinatarios principales.</span><span class="sxs-lookup"><span data-stu-id="45cac-126">Although the Sent hint was not present, the client detected that the task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="45cac-127">Reserved</span><span class="sxs-lookup"><span data-stu-id="45cac-127">Reserved</span></span>  <br/> |<span data-ttu-id="45cac-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="45cac-128">0x00000004</span></span>  <br/> |<span data-ttu-id="45cac-129">Este valor está reservado.</span><span class="sxs-lookup"><span data-stu-id="45cac-129">This value is reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="45cac-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="45cac-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45cac-131">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="45cac-131">Protocol specifications</span></span>

<span data-ttu-id="45cac-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45cac-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45cac-133">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="45cac-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45cac-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45cac-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45cac-135">Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="45cac-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45cac-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="45cac-136">Header files</span></span>

<span data-ttu-id="45cac-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45cac-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="45cac-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="45cac-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45cac-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="45cac-139">See also</span></span>



[<span data-ttu-id="45cac-140">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="45cac-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45cac-141">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="45cac-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45cac-142">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="45cac-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45cac-143">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="45cac-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

