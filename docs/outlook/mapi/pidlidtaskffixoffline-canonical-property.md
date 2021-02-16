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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303041"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a><span data-ttu-id="fba95-103">Propiedad canónica PidLidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="fba95-103">PidLidTaskFFixOffline Canonical Property</span></span>

  
  
<span data-ttu-id="fba95-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fba95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fba95-105">Indica la precisión de la propiedad **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fba95-105">Indicates the accuracy of the **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fba95-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fba95-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fba95-107">dispidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="fba95-107">dispidTaskFFixOffline</span></span>  <br/> |
|<span data-ttu-id="fba95-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="fba95-108">Property set:</span></span>  <br/> |<span data-ttu-id="fba95-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="fba95-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="fba95-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="fba95-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fba95-111">0x0000812C</span><span class="sxs-lookup"><span data-stu-id="fba95-111">0x0000812C</span></span>  <br/> |
|<span data-ttu-id="fba95-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fba95-112">Data type:</span></span>  <br/> |<span data-ttu-id="fba95-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="fba95-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="fba95-114">Área:</span><span class="sxs-lookup"><span data-stu-id="fba95-114">Area:</span></span>  <br/> |<span data-ttu-id="fba95-115">Task</span><span class="sxs-lookup"><span data-stu-id="fba95-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fba95-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fba95-116">Remarks</span></span>

<span data-ttu-id="fba95-117">Si la **propiedad dispidTaskFFixOffline** se establece en FALSE o no está establecida, el valor de la propiedad **dispidTaskOwner** es correcto.</span><span class="sxs-lookup"><span data-stu-id="fba95-117">If the **dispidTaskFFixOffline** property is set to FALSE or is unset, the value for the **dispidTaskOwner** property is correct.</span></span> <span data-ttu-id="fba95-118">Si **dispidTaskFFixOffline** se establece en TRUE, el cliente no puede determinar un valor preciso para **dispidTaskOwner**.</span><span class="sxs-lookup"><span data-stu-id="fba95-118">If **dispidTaskFFixOffline** is set to TRUE, the client cannot determine an accurate value for **dispidTaskOwner**.</span></span> <span data-ttu-id="fba95-119">En ese caso, el cliente puede establecer **dispidTaskOwner en** un nombre de propietario genérico, como "Desconocido".</span><span class="sxs-lookup"><span data-stu-id="fba95-119">In that case, the client can set **dispidTaskOwner** to a generic owner name, such as "Unknown".</span></span> <span data-ttu-id="fba95-120">Sin embargo, si un cliente encuentra un valor **dispidTaskFFixOffline** de TRUE y puede determinar un nombre de propietario preciso, el cliente debe actualizar **dispidTaskOwner** y establecer **dispidTaskFFixOffline** en FALSE.</span><span class="sxs-lookup"><span data-stu-id="fba95-120">However, if a client encounters a **dispidTaskFFixOffline** value of TRUE and can determine an accurate owner name, the client should update **dispidTaskOwner** and set **dispidTaskFFixOffline** to FALSE.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fba95-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fba95-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fba95-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="fba95-122">Protocol specifications</span></span>

<span data-ttu-id="fba95-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fba95-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fba95-124">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="fba95-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fba95-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fba95-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fba95-126">Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="fba95-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="fba95-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fba95-127">Header files</span></span>

<span data-ttu-id="fba95-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fba95-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="fba95-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fba95-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fba95-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fba95-130">See also</span></span>



[<span data-ttu-id="fba95-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fba95-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fba95-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="fba95-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fba95-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fba95-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fba95-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="fba95-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

