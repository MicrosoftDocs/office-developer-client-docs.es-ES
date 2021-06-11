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
ms.openlocfilehash: a64008da93584529916a9303176bba0aa08d3fac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357963"
---
# <a name="pidlidtaskordinal-canonical-property"></a><span data-ttu-id="66dcc-103">Propiedad canónica PidLidTaskOrdinal</span><span class="sxs-lookup"><span data-stu-id="66dcc-103">PidLidTaskOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="66dcc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66dcc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66dcc-105">Proporciona una ayuda a las tareas de ordenación personalizadas.</span><span class="sxs-lookup"><span data-stu-id="66dcc-105">Provides an aid to custom sorting tasks.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="66dcc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="66dcc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="66dcc-107">dispidTaskOrdinal</span><span class="sxs-lookup"><span data-stu-id="66dcc-107">dispidTaskOrdinal</span></span>  <br/> |
|<span data-ttu-id="66dcc-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="66dcc-108">Property set:</span></span>  <br/> |<span data-ttu-id="66dcc-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="66dcc-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="66dcc-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="66dcc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="66dcc-111">0x00008123</span><span class="sxs-lookup"><span data-stu-id="66dcc-111">0x00008123</span></span>  <br/> |
|<span data-ttu-id="66dcc-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="66dcc-112">Data type:</span></span>  <br/> |<span data-ttu-id="66dcc-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="66dcc-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="66dcc-114">Área:</span><span class="sxs-lookup"><span data-stu-id="66dcc-114">Area:</span></span>  <br/> |<span data-ttu-id="66dcc-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="66dcc-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66dcc-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="66dcc-116">Remarks</span></span>

<span data-ttu-id="66dcc-117">Es posible que esta propiedad se desajunte.</span><span class="sxs-lookup"><span data-stu-id="66dcc-117">This property may be left unset.</span></span> <span data-ttu-id="66dcc-118">Si se establece, su valor debe ser mayor que "0x800186A0" (-2.147.383.648) y menor que "0x7FFE7960" (2.147.383.648) y debe ser único entre las tareas de la misma carpeta.</span><span class="sxs-lookup"><span data-stu-id="66dcc-118">If set, its value must be greater than "0x800186A0" (-2,147,383,648) and less than "0x7FFE7960" (2,147,383,648) and must be unique among tasks in the same folder.</span></span>
  
<span data-ttu-id="66dcc-119">Siempre que el cliente establece esta propiedad en un número menor que el negativo del valor actual de la propiedad  **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) de la carpeta, el cliente también debe actualizar PR_ORDINAL_MOST en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="66dcc-119">Whenever the client sets this property to a number less than the negative of the current value of the **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) property of the folder, the client must also update **PR_ORDINAL_MOST** on the folder.</span></span> 
  
<span data-ttu-id="66dcc-120">La **PR_ORDINAL_MOST** de la carpeta proporciona una forma eficaz de determinar un valor único entre las tareas de la misma carpeta.</span><span class="sxs-lookup"><span data-stu-id="66dcc-120">The **PR_ORDINAL_MOST** property of the folder provides an efficient way to determine a unique value among tasks in the same folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="66dcc-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="66dcc-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="66dcc-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="66dcc-122">Protocol specifications</span></span>

<span data-ttu-id="66dcc-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66dcc-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66dcc-124">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="66dcc-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="66dcc-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66dcc-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66dcc-126">Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="66dcc-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="66dcc-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="66dcc-127">Header files</span></span>

<span data-ttu-id="66dcc-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66dcc-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="66dcc-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="66dcc-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="66dcc-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="66dcc-130">See also</span></span>



[<span data-ttu-id="66dcc-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="66dcc-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="66dcc-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="66dcc-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="66dcc-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="66dcc-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="66dcc-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="66dcc-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

