---
title: Propiedad canónica PidLidTaskOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOrdinal
api_type:
- COM
ms.assetid: 1021860e-4c40-4c22-aa68-b568d046aaf7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 033bc038988373b11f3eac863a256717624999f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818979"
---
# <a name="pidlidtaskordinal-canonical-property"></a><span data-ttu-id="37921-103">Propiedad canónica PidLidTaskOrdinal</span><span class="sxs-lookup"><span data-stu-id="37921-103">PidLidTaskOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="37921-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="37921-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="37921-105">Proporciona ayuda para las tareas de ordenación personalizadas.</span><span class="sxs-lookup"><span data-stu-id="37921-105">Provides an aid to custom sorting tasks.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37921-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="37921-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37921-107">dispidTaskOrdinal</span><span class="sxs-lookup"><span data-stu-id="37921-107">dispidTaskOrdinal</span></span>  <br/> |
|<span data-ttu-id="37921-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="37921-108">Property set:</span></span>  <br/> |<span data-ttu-id="37921-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="37921-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="37921-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="37921-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="37921-111">0x00008123</span><span class="sxs-lookup"><span data-stu-id="37921-111">0x00008123</span></span>  <br/> |
|<span data-ttu-id="37921-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="37921-112">Data type:</span></span>  <br/> |<span data-ttu-id="37921-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="37921-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="37921-114">Área:</span><span class="sxs-lookup"><span data-stu-id="37921-114">Area:</span></span>  <br/> |<span data-ttu-id="37921-115">Task</span><span class="sxs-lookup"><span data-stu-id="37921-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37921-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37921-116">Remarks</span></span>

<span data-ttu-id="37921-117">Esta propiedad se puede dejar sin establecer.</span><span class="sxs-lookup"><span data-stu-id="37921-117">This property may be left unset.</span></span> <span data-ttu-id="37921-118">Si se establece, su valor debe ser mayor que "0x800186A0" (-2,147,383,648) y menor que "0x7FFE7960" (2,147,383,648) y debe ser único entre las tareas en la misma carpeta.</span><span class="sxs-lookup"><span data-stu-id="37921-118">If set, its value must be greater than "0x800186A0" (-2,147,383,648) and less than "0x7FFE7960" (2,147,383,648) and must be unique among tasks in the same folder.</span></span>
  
<span data-ttu-id="37921-119">Cada vez que el cliente establece esta propiedad en un número menor que el valor negativo del valor actual de la propiedad **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) de la carpeta, el cliente también debe actualizar **PR_ORDINAL_MOST** en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="37921-119">Whenever the client sets this property to a number less than the negative of the current value of the **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) property of the folder, the client must also update **PR_ORDINAL_MOST** on the folder.</span></span> 
  
<span data-ttu-id="37921-120">La propiedad **PR_ORDINAL_MOST** de la carpeta proporciona una manera eficaz para determinar un valor único entre tareas en la misma carpeta.</span><span class="sxs-lookup"><span data-stu-id="37921-120">The **PR_ORDINAL_MOST** property of the folder provides an efficient way to determine a unique value among tasks in the same folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="37921-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="37921-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="37921-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="37921-122">Protocol specifications</span></span>

<span data-ttu-id="37921-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37921-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37921-124">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="37921-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="37921-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37921-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37921-126">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="37921-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="37921-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="37921-127">Header files</span></span>

<span data-ttu-id="37921-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="37921-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="37921-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="37921-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37921-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="37921-130">See also</span></span>



[<span data-ttu-id="37921-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="37921-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="37921-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="37921-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="37921-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="37921-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="37921-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="37921-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

