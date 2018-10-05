---
title: Propiedad canónica PidLidTaskFFixOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFFixOffline
api_type:
- COM
ms.assetid: bbaf7df4-2de0-4da3-9125-eb24dfa94cd8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 226e59ef6aa88bc290cf5aeb4d620979f926e1eb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386267"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a><span data-ttu-id="4f649-103">Propiedad canónica PidLidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="4f649-103">PidLidTaskFFixOffline Canonical Property</span></span>

  
  
<span data-ttu-id="4f649-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f649-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f649-105">Indica la precisión de la propiedad **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4f649-105">Indicates the accuracy of the **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4f649-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4f649-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f649-107">dispidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="4f649-107">dispidTaskFFixOffline</span></span>  <br/> |
|<span data-ttu-id="4f649-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="4f649-108">Property set:</span></span>  <br/> |<span data-ttu-id="4f649-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="4f649-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="4f649-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="4f649-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4f649-111">0x0000812C</span><span class="sxs-lookup"><span data-stu-id="4f649-111">0x0000812C</span></span>  <br/> |
|<span data-ttu-id="4f649-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4f649-112">Data type:</span></span>  <br/> |<span data-ttu-id="4f649-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4f649-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4f649-114">Área:</span><span class="sxs-lookup"><span data-stu-id="4f649-114">Area:</span></span>  <br/> |<span data-ttu-id="4f649-115">Task</span><span class="sxs-lookup"><span data-stu-id="4f649-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f649-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4f649-116">Remarks</span></span>

<span data-ttu-id="4f649-117">Si la propiedad **dispidTaskFFixOffline** está establecida en FALSE o no está establecida, el valor de la propiedad **dispidTaskOwner** es correcto.</span><span class="sxs-lookup"><span data-stu-id="4f649-117">If the **dispidTaskFFixOffline** property is set to FALSE or is unset, the value for the **dispidTaskOwner** property is correct.</span></span> <span data-ttu-id="4f649-118">Si **dispidTaskFFixOffline** está establecida en TRUE, el cliente no puede determinar un valor exacto para **dispidTaskOwner**.</span><span class="sxs-lookup"><span data-stu-id="4f649-118">If **dispidTaskFFixOffline** is set to TRUE, the client cannot determine an accurate value for **dispidTaskOwner**.</span></span> <span data-ttu-id="4f649-119">En ese caso, el cliente puede establecer **dispidTaskOwner** a un nombre de propietario genérico, como "Unknown".</span><span class="sxs-lookup"><span data-stu-id="4f649-119">In that case, the client can set **dispidTaskOwner** to a generic owner name, such as "Unknown".</span></span> <span data-ttu-id="4f649-120">Sin embargo, si un cliente encuentra **dispidTaskFFixOffline** el valor TRUE y puede determinar un nombre de propietario precisos, el cliente debe actualizar **dispidTaskOwner** y establece **dispidTaskFFixOffline** en FALSE.</span><span class="sxs-lookup"><span data-stu-id="4f649-120">However, if a client encounters a **dispidTaskFFixOffline** value of TRUE and can determine an accurate owner name, the client should update **dispidTaskOwner** and set **dispidTaskFFixOffline** to FALSE.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4f649-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f649-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4f649-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="4f649-122">Protocol specifications</span></span>

<span data-ttu-id="4f649-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f649-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f649-124">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4f649-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4f649-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f649-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f649-126">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="4f649-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="4f649-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4f649-127">Header files</span></span>

<span data-ttu-id="4f649-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f649-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f649-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4f649-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f649-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f649-130">See also</span></span>



[<span data-ttu-id="4f649-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4f649-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f649-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4f649-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f649-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4f649-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f649-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="4f649-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

