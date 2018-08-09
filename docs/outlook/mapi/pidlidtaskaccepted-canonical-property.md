---
title: Propiedad canónica PidLidTaskAccepted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAccepted
api_type:
- COM
ms.assetid: 8e31f893-b639-43da-a535-662153c82d82
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7448768a0a35cbf53b481eab0571b405fead1544
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818950"
---
# <a name="pidlidtaskaccepted-canonical-property"></a><span data-ttu-id="878ae-103">Propiedad canónica PidLidTaskAccepted</span><span class="sxs-lookup"><span data-stu-id="878ae-103">PidLidTaskAccepted Canonical Property</span></span>

  
  
<span data-ttu-id="878ae-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="878ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="878ae-105">Indica si un usuario asignado a la tarea respondió a una solicitud de tarea.</span><span class="sxs-lookup"><span data-stu-id="878ae-105">Indicates whether a task assignee has replied to a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="878ae-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="878ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="878ae-107">dispidTaskAccepted</span><span class="sxs-lookup"><span data-stu-id="878ae-107">dispidTaskAccepted</span></span>  <br/> |
|<span data-ttu-id="878ae-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="878ae-108">Property set:</span></span>  <br/> |<span data-ttu-id="878ae-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="878ae-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="878ae-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="878ae-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="878ae-111">0x00008108</span><span class="sxs-lookup"><span data-stu-id="878ae-111">0x00008108</span></span>  <br/> |
|<span data-ttu-id="878ae-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="878ae-112">Data type:</span></span>  <br/> |<span data-ttu-id="878ae-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="878ae-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="878ae-114">Área:</span><span class="sxs-lookup"><span data-stu-id="878ae-114">Area:</span></span>  <br/> |<span data-ttu-id="878ae-115">Task</span><span class="sxs-lookup"><span data-stu-id="878ae-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="878ae-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="878ae-116">Remarks</span></span>

<span data-ttu-id="878ae-117">El cliente establece esta propiedad en FALSE para una nueva tarea o el cliente establece esta propiedad en TRUE cuando se acepta o rechaza una tarea.</span><span class="sxs-lookup"><span data-stu-id="878ae-117">The client sets this property to FALSE for a new task, or the client sets this property to TRUE when a task is either accepted or rejected.</span></span> <span data-ttu-id="878ae-118">Si la propiedad se deja sin establecer, se supone un valor FALSE.</span><span class="sxs-lookup"><span data-stu-id="878ae-118">If the property is left unset, a value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="878ae-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="878ae-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="878ae-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="878ae-120">Protocol specifications</span></span>

<span data-ttu-id="878ae-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="878ae-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="878ae-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="878ae-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="878ae-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="878ae-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="878ae-124">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="878ae-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="878ae-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="878ae-125">Header files</span></span>

<span data-ttu-id="878ae-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="878ae-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="878ae-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="878ae-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="878ae-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="878ae-128">See also</span></span>



[<span data-ttu-id="878ae-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="878ae-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="878ae-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="878ae-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="878ae-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="878ae-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="878ae-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="878ae-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

