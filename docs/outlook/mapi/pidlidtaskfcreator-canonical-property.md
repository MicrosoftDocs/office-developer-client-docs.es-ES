---
title: Propiedad canónica PidLidTaskFCreator
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dfb49fafcc2dc368e84786b526869e0447ccaf8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303083"
---
# <a name="pidlidtaskfcreator-canonical-property"></a><span data-ttu-id="0fb24-103">Propiedad canónica PidLidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="0fb24-103">PidLidTaskFCreator Canonical Property</span></span>

  
  
<span data-ttu-id="0fb24-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fb24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fb24-105">Indica que la tarea se creó originalmente por el agente de usuario o usuario actual en lugar de mediante el procesamiento de una solicitud de tarea.</span><span class="sxs-lookup"><span data-stu-id="0fb24-105">Indicates the task was originally created by the current user or user agent instead of by processing a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0fb24-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0fb24-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0fb24-107">dispidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="0fb24-107">dispidTaskFCreator</span></span>  <br/> |
|<span data-ttu-id="0fb24-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="0fb24-108">Property set:</span></span>  <br/> |<span data-ttu-id="0fb24-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="0fb24-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="0fb24-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="0fb24-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0fb24-111">0x0000811E</span><span class="sxs-lookup"><span data-stu-id="0fb24-111">0x0000811E</span></span>  <br/> |
|<span data-ttu-id="0fb24-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0fb24-112">Data type:</span></span>  <br/> |<span data-ttu-id="0fb24-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0fb24-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0fb24-114">Área:</span><span class="sxs-lookup"><span data-stu-id="0fb24-114">Area:</span></span>  <br/> |<span data-ttu-id="0fb24-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="0fb24-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0fb24-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0fb24-116">Remarks</span></span>

<span data-ttu-id="0fb24-117">El cliente establece esta propiedad en TRUE cuando el usuario crea la tarea y en FALSE cuando la tarea está asignada por otro usuario.</span><span class="sxs-lookup"><span data-stu-id="0fb24-117">The client sets this property to TRUE when the user creates the task and to FALSE when the task is assigned by another user.</span></span> <span data-ttu-id="0fb24-118">Si esta propiedad se deja no establecida, se presupone un valor de TRUE.</span><span class="sxs-lookup"><span data-stu-id="0fb24-118">If this property is left unset, a value of TRUE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0fb24-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0fb24-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0fb24-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0fb24-120">Protocol specifications</span></span>

<span data-ttu-id="0fb24-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fb24-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fb24-122">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0fb24-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0fb24-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fb24-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fb24-124">Define varios objetos que modelan el equivalente electrónico de tareas, asignaciones de tareas y actualizaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="0fb24-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0fb24-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0fb24-125">Header files</span></span>

<span data-ttu-id="0fb24-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0fb24-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0fb24-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0fb24-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0fb24-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fb24-128">See also</span></span>



[<span data-ttu-id="0fb24-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0fb24-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0fb24-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="0fb24-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0fb24-131">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0fb24-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0fb24-132">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="0fb24-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

