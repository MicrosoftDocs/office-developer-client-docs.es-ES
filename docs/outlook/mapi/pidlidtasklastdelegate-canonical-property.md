---
title: Propiedad canónica PidLidTaskLastDelegate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastDelegate
api_type:
- COM
ms.assetid: 5eb8c1ce-063f-4273-acba-e6f9c994e7d3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ddf4b81ed35f500dad0029ea6375e9a75a996186
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355674"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a><span data-ttu-id="9f60d-103">Propiedad canónica PidLidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="9f60d-103">PidLidTaskLastDelegate Canonical Property</span></span>

  
  
<span data-ttu-id="9f60d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f60d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9f60d-105">Asigna un nombre al usuario que se asignó o a quien se asignó la tarea más recientemente.</span><span class="sxs-lookup"><span data-stu-id="9f60d-105">Names the user who most recently assigned or was assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f60d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9f60d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9f60d-107">dispidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="9f60d-107">dispidTaskLastDelegate</span></span>  <br/> |
|<span data-ttu-id="9f60d-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="9f60d-108">Property set:</span></span>  <br/> |<span data-ttu-id="9f60d-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="9f60d-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="9f60d-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="9f60d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9f60d-111">0x00008125</span><span class="sxs-lookup"><span data-stu-id="9f60d-111">0x00008125</span></span>  <br/> |
|<span data-ttu-id="9f60d-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9f60d-112">Data type:</span></span>  <br/> |<span data-ttu-id="9f60d-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9f60d-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9f60d-114">Área:</span><span class="sxs-lookup"><span data-stu-id="9f60d-114">Area:</span></span>  <br/> |<span data-ttu-id="9f60d-115">Task</span><span class="sxs-lookup"><span data-stu-id="9f60d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f60d-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f60d-116">Remarks</span></span>

<span data-ttu-id="9f60d-117">Antes de enviar una solicitud de tarea, el cliente establece esta propiedad en el nombre del asignador de tareas.</span><span class="sxs-lookup"><span data-stu-id="9f60d-117">Before sending a task request, the client sets this property to the name of the task assigner.</span></span> <span data-ttu-id="9f60d-118">Antes de enviar una respuesta de tarea, el cliente establece esta propiedad en el nombre del usuario al que se asigna la tarea.</span><span class="sxs-lookup"><span data-stu-id="9f60d-118">Before sending a task response, the client sets this property to the name of the task assignee.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9f60d-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9f60d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9f60d-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="9f60d-120">Protocol specifications</span></span>

<span data-ttu-id="9f60d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f60d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f60d-122">Proporciona la definición del conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="9f60d-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9f60d-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f60d-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f60d-124">Define varios objetos que modela el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="9f60d-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9f60d-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9f60d-125">Header files</span></span>

<span data-ttu-id="9f60d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9f60d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9f60d-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9f60d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f60d-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9f60d-128">See also</span></span>



[<span data-ttu-id="9f60d-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9f60d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9f60d-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="9f60d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9f60d-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9f60d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9f60d-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="9f60d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

