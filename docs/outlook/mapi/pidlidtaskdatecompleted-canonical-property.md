---
title: Propiedad canónica PidLidTaskDateCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDateCompleted
api_type:
- COM
ms.assetid: ae384529-55e2-4da1-9a41-acc292591a7c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9737b5f940f95c88c2d3c5c6e98fc885daf64219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818929"
---
# <a name="pidlidtaskdatecompleted-canonical-property"></a><span data-ttu-id="ecc50-103">Propiedad canónica PidLidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="ecc50-103">PidLidTaskDateCompleted Canonical Property</span></span>

  
  
<span data-ttu-id="ecc50-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ecc50-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ecc50-105">Especifica la fecha cuando el usuario complete la tarea.</span><span class="sxs-lookup"><span data-stu-id="ecc50-105">Specifies the date when the user completes the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ecc50-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ecc50-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ecc50-107">dispidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="ecc50-107">dispidTaskDateCompleted</span></span>  <br/> |
|<span data-ttu-id="ecc50-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="ecc50-108">Property set:</span></span>  <br/> |<span data-ttu-id="ecc50-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="ecc50-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="ecc50-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="ecc50-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ecc50-111">0x0000810F</span><span class="sxs-lookup"><span data-stu-id="ecc50-111">0x0000810F</span></span>  <br/> |
|<span data-ttu-id="ecc50-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ecc50-112">Data type:</span></span>  <br/> |<span data-ttu-id="ecc50-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ecc50-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ecc50-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ecc50-114">Area:</span></span>  <br/> |<span data-ttu-id="ecc50-115">Task</span><span class="sxs-lookup"><span data-stu-id="ecc50-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecc50-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ecc50-116">Remarks</span></span>

<span data-ttu-id="ecc50-117">Si se establece, esta propiedad debe tener un componente de hora de la medianoche en la zona horaria local, convertir a hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="ecc50-117">If set, this property must have a time component of midnight in the local time zone, converted to Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ecc50-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ecc50-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ecc50-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="ecc50-119">Protocol specifications</span></span>

<span data-ttu-id="ecc50-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecc50-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecc50-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ecc50-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ecc50-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecc50-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecc50-123">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="ecc50-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="ecc50-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ecc50-124">Header files</span></span>

<span data-ttu-id="ecc50-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ecc50-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ecc50-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ecc50-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ecc50-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecc50-127">See also</span></span>



[<span data-ttu-id="ecc50-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ecc50-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ecc50-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="ecc50-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ecc50-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ecc50-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ecc50-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="ecc50-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

