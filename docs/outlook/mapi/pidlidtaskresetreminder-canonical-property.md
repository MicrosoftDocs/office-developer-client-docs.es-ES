---
title: Propiedad canónica PidLidTaskResetReminder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskResetReminder
api_type:
- COM
ms.assetid: f6da69ff-a913-4a65-bb07-8ad3c5685e5e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9a438fb2b1862d44905a63fda3e5f68b7878cd99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316621"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a><span data-ttu-id="af46e-103">Propiedad canónica PidLidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="af46e-103">PidLidTaskResetReminder Canonical Property</span></span>

  
  
<span data-ttu-id="af46e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af46e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af46e-105">Indica si las instancias futuras de tareas periódicas necesitan avisos, aunque **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) es FALSE.</span><span class="sxs-lookup"><span data-stu-id="af46e-105">Indicates whether future instances of recurring tasks need reminders, even though **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) is FALSE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="af46e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="af46e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af46e-107">dispidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="af46e-107">dispidTaskResetReminder</span></span>  <br/> |
|<span data-ttu-id="af46e-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="af46e-108">Property set:</span></span>  <br/> |<span data-ttu-id="af46e-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="af46e-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="af46e-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="af46e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="af46e-111">0x00008107</span><span class="sxs-lookup"><span data-stu-id="af46e-111">0x00008107</span></span>  <br/> |
|<span data-ttu-id="af46e-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="af46e-112">Data type:</span></span>  <br/> |<span data-ttu-id="af46e-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="af46e-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="af46e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="af46e-114">Area:</span></span>  <br/> |<span data-ttu-id="af46e-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="af46e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af46e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="af46e-116">Remarks</span></span>

<span data-ttu-id="af46e-117">Este valor se establece en TRUE cuando se descarta el aviso de la tarea y se establece en FALSE en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="af46e-117">This value is set to TRUE when the task's reminder is dismissed, and set to FALSE otherwise.</span></span> <span data-ttu-id="af46e-118">Si se deja sin conjunto, se presupone un valor predeterminado de FALSE.</span><span class="sxs-lookup"><span data-stu-id="af46e-118">If left unset, a default of FALSE is assumed.</span></span>
  
<span data-ttu-id="af46e-119">Como se especifica en [[MS-OXORMDR],](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)la propiedad **dispidReminderSet** indica si se establece un aviso en la tarea.</span><span class="sxs-lookup"><span data-stu-id="af46e-119">As specified in [[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), the **dispidReminderSet** property indicates whether a reminder is set on the task.</span></span> <span data-ttu-id="af46e-120">Sin embargo, esta propiedad solo indica la presencia de un aviso en una sola tarea.</span><span class="sxs-lookup"><span data-stu-id="af46e-120">However, this property only indicates the presence of a reminder on a single task.</span></span> <span data-ttu-id="af46e-121">No se puede usar solo para determinar si una instancia futura de una tarea periódica necesita un aviso.</span><span class="sxs-lookup"><span data-stu-id="af46e-121">It cannot be used alone to determine whether a future instance of a recurring task needs a reminder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="af46e-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="af46e-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af46e-123">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="af46e-123">Protocol specifications</span></span>

<span data-ttu-id="af46e-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af46e-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af46e-125">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="af46e-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="af46e-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af46e-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af46e-127">Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="af46e-127">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="af46e-128">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af46e-128">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af46e-129">Especifica las propiedades y el modelo de interacción para el correo electrónico y otros avisos de objetos.</span><span class="sxs-lookup"><span data-stu-id="af46e-129">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="af46e-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="af46e-130">Header files</span></span>

<span data-ttu-id="af46e-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af46e-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="af46e-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="af46e-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af46e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="af46e-133">See also</span></span>



[<span data-ttu-id="af46e-134">Propiedad can�nico de PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="af46e-134">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)


[<span data-ttu-id="af46e-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="af46e-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af46e-136">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="af46e-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af46e-137">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="af46e-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af46e-138">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="af46e-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

