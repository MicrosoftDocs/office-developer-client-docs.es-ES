---
title: Propiedad canónica PidLidTaskVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskVersion
api_type:
- COM
ms.assetid: 3ab77f25-ad11-4501-8d35-ef560c07e2f2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 38bcf40f24cc7901ebcbb60a099dc0e797d8e4b8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588037"
---
# <a name="pidlidtaskversion-canonical-property"></a><span data-ttu-id="1ed3d-103">Propiedad canónica PidLidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="1ed3d-103">PidLidTaskVersion Canonical Property</span></span>

  
  
<span data-ttu-id="1ed3d-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ed3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ed3d-105">Indica qué copia es la actualización más reciente de una tarea.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-105">Indicates which copy is the latest update of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1ed3d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1ed3d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1ed3d-107">dispidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="1ed3d-107">dispidTaskVersion</span></span>  <br/> |
|<span data-ttu-id="1ed3d-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="1ed3d-108">Property set:</span></span>  <br/> |<span data-ttu-id="1ed3d-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="1ed3d-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="1ed3d-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="1ed3d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1ed3d-111">0x00008112</span><span class="sxs-lookup"><span data-stu-id="1ed3d-111">0x00008112</span></span>  <br/> |
|<span data-ttu-id="1ed3d-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1ed3d-112">Data type:</span></span>  <br/> |<span data-ttu-id="1ed3d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1ed3d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1ed3d-114">Área:</span><span class="sxs-lookup"><span data-stu-id="1ed3d-114">Area:</span></span>  <br/> |<span data-ttu-id="1ed3d-115">Task</span><span class="sxs-lookup"><span data-stu-id="1ed3d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ed3d-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ed3d-116">Remarks</span></span>

<span data-ttu-id="1ed3d-117">Se omiten las actualizaciones con versiones inferiores a la tarea.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-117">Updates with lower versions than the task are ignored.</span></span> 
  
<span data-ttu-id="1ed3d-118">Incrustación de una tarea en una comunicación de la tarea, el cliente establece la versión actual de la tarea incrustada en así como la comunicación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-118">When embedding a task in a task communication, the client sets the current version of the embedded task on the task communication as well.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1ed3d-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ed3d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1ed3d-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1ed3d-120">Protocol specifications</span></span>

<span data-ttu-id="1ed3d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ed3d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1ed3d-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1ed3d-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ed3d-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1ed3d-124">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1ed3d-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1ed3d-125">Header files</span></span>

<span data-ttu-id="1ed3d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ed3d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1ed3d-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1ed3d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ed3d-128">See also</span></span>



[<span data-ttu-id="1ed3d-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1ed3d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1ed3d-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1ed3d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1ed3d-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1ed3d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1ed3d-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="1ed3d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

