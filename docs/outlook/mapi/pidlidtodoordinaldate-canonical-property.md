---
title: Propiedad canónica PidLidToDoOrdinalDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoOrdinalDate
api_type:
- COM
ms.assetid: b6a500fc-07f4-4788-ae46-d179a96a48e2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b0c5e3019efeeb0b9788d81e8730e976bfcc9d75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345279"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a><span data-ttu-id="17299-103">Propiedad canónica PidLidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="17299-103">PidLidToDoOrdinalDate Canonical Property</span></span>

  
  
<span data-ttu-id="17299-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17299-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17299-105">Determina el criterio de ordenación de los objetos en una lista de tareas pendientes consolidada.</span><span class="sxs-lookup"><span data-stu-id="17299-105">Determines the sort order of objects in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="17299-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="17299-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="17299-107">dispidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="17299-107">dispidToDoOrdinalDate</span></span>  <br/> |
|<span data-ttu-id="17299-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="17299-108">Property set:</span></span>  <br/> |<span data-ttu-id="17299-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="17299-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="17299-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="17299-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="17299-111">0x000085A0</span><span class="sxs-lookup"><span data-stu-id="17299-111">0x000085A0</span></span>  <br/> |
|<span data-ttu-id="17299-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="17299-112">Data type:</span></span>  <br/> |<span data-ttu-id="17299-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="17299-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="17299-114">Área:</span><span class="sxs-lookup"><span data-stu-id="17299-114">Area:</span></span>  <br/> |<span data-ttu-id="17299-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="17299-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17299-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="17299-116">Remarks</span></span>

<span data-ttu-id="17299-117">Cuando se marca un objeto, esta propiedad se debe establecer en la hora actual en la hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="17299-117">When an object is flagged, this property should be set to the current time in Coordinated Universal Time (UTC).</span></span> 
  
<span data-ttu-id="17299-118">Si el cliente permite a un usuario reordenar las tareas dentro de la lista de tareas consolidadas mediante el arrastre o con otros mecanismos, puede usar cualquier algoritmo adecuado para determinar el nuevo valor de esta propiedad de modo que la tarea aparezca en el punto correcto cuando se use esta propiedad como Sor campo de nota.</span><span class="sxs-lookup"><span data-stu-id="17299-118">If the client allows a user to reorder tasks within the consolidated task list via dragging or other mechanisms, they can use any suitable algorithm to determine the new value of this property so that the task appears in the correct place when this property is used as a sorting field.</span></span>
  
<span data-ttu-id="17299-119">Cuando se usa esta propiedad para ordenar objetos y el orden resulta en un empate, la propiedad **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) se usa como un disyuntor.</span><span class="sxs-lookup"><span data-stu-id="17299-119">When this property is used to sort objects and the sort results in a tie, the **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) property is used as a tie breaker.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="17299-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="17299-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="17299-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="17299-121">Protocol specifications</span></span>

<span data-ttu-id="17299-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17299-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17299-123">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="17299-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="17299-124">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17299-124">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17299-125">Especifica las propiedades y operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="17299-125">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="17299-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="17299-126">Header files</span></span>

<span data-ttu-id="17299-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="17299-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="17299-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="17299-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17299-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="17299-129">See also</span></span>



[<span data-ttu-id="17299-130">Propiedad canónica PidLidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="17299-130">PidLidToDoSubOrdinal Canonical Property</span></span>](pidlidtodosubordinal-canonical-property.md)


[<span data-ttu-id="17299-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="17299-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="17299-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="17299-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="17299-133">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="17299-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="17299-134">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="17299-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

