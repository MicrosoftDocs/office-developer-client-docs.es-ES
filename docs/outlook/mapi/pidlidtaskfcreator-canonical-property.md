---
title: Propiedad canónico PidLidTaskFCreator
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFCreator
api_type:
- COM
ms.assetid: bb88750b-4773-4241-aa38-462a2634dbcb
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 458a20e238d6023520ede3416ece239f2d553891
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818965"
---
# <a name="pidlidtaskfcreator-canonical-property"></a><span data-ttu-id="525c7-103">Propiedad canónico PidLidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="525c7-103">PidLidTaskFCreator Canonical Property</span></span>

  
  
<span data-ttu-id="525c7-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="525c7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="525c7-105">Indica que la tarea se creó originalmente por el usuario actual o el agente de usuario en lugar de hacerlo mediante el procesamiento de una solicitud de tarea.</span><span class="sxs-lookup"><span data-stu-id="525c7-105">Indicates the task was originally created by the current user or user agent instead of by processing a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="525c7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="525c7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="525c7-107">dispidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="525c7-107">dispidTaskFCreator</span></span>  <br/> |
|<span data-ttu-id="525c7-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="525c7-108">Property set:</span></span>  <br/> |<span data-ttu-id="525c7-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="525c7-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="525c7-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="525c7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="525c7-111">0x0000811E</span><span class="sxs-lookup"><span data-stu-id="525c7-111">0x0000811E</span></span>  <br/> |
|<span data-ttu-id="525c7-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="525c7-112">Data type:</span></span>  <br/> |<span data-ttu-id="525c7-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="525c7-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="525c7-114">Área:</span><span class="sxs-lookup"><span data-stu-id="525c7-114">Area:</span></span>  <br/> |<span data-ttu-id="525c7-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="525c7-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="525c7-116">Notas</span><span class="sxs-lookup"><span data-stu-id="525c7-116">Remarks</span></span>

<span data-ttu-id="525c7-117">El cliente establece esta propiedad en TRUE cuando el usuario crea la tarea y en FALSE cuando se asigna la tarea por otro usuario.</span><span class="sxs-lookup"><span data-stu-id="525c7-117">The client sets this property to TRUE when the user creates the task and to FALSE when the task is assigned by another user.</span></span> <span data-ttu-id="525c7-118">Si esta propiedad se deja sin establecer, se supone un valor de TRUE.</span><span class="sxs-lookup"><span data-stu-id="525c7-118">If this property is left unset, a value of TRUE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="525c7-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="525c7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="525c7-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="525c7-120">Protocol specifications</span></span>

<span data-ttu-id="525c7-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="525c7-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="525c7-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="525c7-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="525c7-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="525c7-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="525c7-124">Define varios objetos que modelar el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="525c7-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="525c7-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="525c7-125">Header files</span></span>

<span data-ttu-id="525c7-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="525c7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="525c7-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="525c7-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="525c7-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="525c7-128">See also</span></span>



[<span data-ttu-id="525c7-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="525c7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="525c7-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="525c7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="525c7-131">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="525c7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="525c7-132">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="525c7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

