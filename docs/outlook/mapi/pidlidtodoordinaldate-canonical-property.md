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
ms.openlocfilehash: d708424ccb15be15746fe8a33eea73a8e0f99323
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819007"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a><span data-ttu-id="b929b-103">Propiedad canónica PidLidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="b929b-103">PidLidToDoOrdinalDate Canonical Property</span></span>

  
  
<span data-ttu-id="b929b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b929b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b929b-105">Determina el criterio de ordenación de objetos en una lista de tareas pendientes consolidada.</span><span class="sxs-lookup"><span data-stu-id="b929b-105">Determines the sort order of objects in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b929b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b929b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b929b-107">dispidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="b929b-107">dispidToDoOrdinalDate</span></span>  <br/> |
|<span data-ttu-id="b929b-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="b929b-108">Property set:</span></span>  <br/> |<span data-ttu-id="b929b-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="b929b-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="b929b-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="b929b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b929b-111">0x000085A0</span><span class="sxs-lookup"><span data-stu-id="b929b-111">0x000085A0</span></span>  <br/> |
|<span data-ttu-id="b929b-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b929b-112">Data type:</span></span>  <br/> |<span data-ttu-id="b929b-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b929b-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b929b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="b929b-114">Area:</span></span>  <br/> |<span data-ttu-id="b929b-115">Task</span><span class="sxs-lookup"><span data-stu-id="b929b-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b929b-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b929b-116">Remarks</span></span>

<span data-ttu-id="b929b-117">Cuando se marca un objeto, esta propiedad debe establecerse en la hora actual en hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="b929b-117">When an object is flagged, this property should be set to the current time in Coordinated Universal Time (UTC).</span></span> 
  
<span data-ttu-id="b929b-118">Si el cliente permite a un usuario cambiar el orden de las tareas de la lista de tareas consolidado a través de arrastrar u otros mecanismos, pueden utilizar cualquier algoritmo adecuado para determinar el nuevo valor de esta propiedad para que la tarea aparezca en el lugar correcto cuando se usa esta propiedad como un ordenar campo Ting.</span><span class="sxs-lookup"><span data-stu-id="b929b-118">If the client allows a user to reorder tasks within the consolidated task list via dragging or other mechanisms, they can use any suitable algorithm to determine the new value of this property so that the task appears in the correct place when this property is used as a sorting field.</span></span>
  
<span data-ttu-id="b929b-119">Cuando esta propiedad se usa para ordenar los objetos y los resultados de ordenación en una placa, se utiliza la propiedad **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) como un separador de placa.</span><span class="sxs-lookup"><span data-stu-id="b929b-119">When this property is used to sort objects and the sort results in a tie, the **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) property is used as a tie breaker.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b929b-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b929b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b929b-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="b929b-121">Protocol specifications</span></span>

<span data-ttu-id="b929b-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b929b-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b929b-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="b929b-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b929b-124">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b929b-124">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b929b-125">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="b929b-125">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b929b-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b929b-126">Header files</span></span>

<span data-ttu-id="b929b-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b929b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b929b-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b929b-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b929b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b929b-129">See also</span></span>



[<span data-ttu-id="b929b-130">Propiedad canónica PidLidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="b929b-130">PidLidToDoSubOrdinal Canonical Property</span></span>](pidlidtodosubordinal-canonical-property.md)


[<span data-ttu-id="b929b-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b929b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b929b-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="b929b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b929b-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b929b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b929b-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="b929b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

