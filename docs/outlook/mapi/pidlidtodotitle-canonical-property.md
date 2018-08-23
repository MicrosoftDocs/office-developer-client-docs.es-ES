---
title: Propiedad canónica PidLidToDoTitle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9973e68dbceea03f31bfc47ede34f004fa3f39b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570418"
---
# <a name="pidlidtodotitle-canonical-property"></a><span data-ttu-id="95da6-103">Propiedad canónica PidLidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="95da6-103">PidLidToDoTitle Canonical Property</span></span>

  
  
<span data-ttu-id="95da6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95da6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95da6-105">Contiene texto puede especificar el usuario para identificar este objeto de mensaje en una lista de tareas pendientes consolidada.</span><span class="sxs-lookup"><span data-stu-id="95da6-105">Contains user-specifiable text to identify this message object in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="95da6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="95da6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="95da6-107">dispidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="95da6-107">dispidToDoTitle</span></span>  <br/> |
|<span data-ttu-id="95da6-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="95da6-108">Property set:</span></span>  <br/> |<span data-ttu-id="95da6-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="95da6-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="95da6-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="95da6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="95da6-111">0x000085A4</span><span class="sxs-lookup"><span data-stu-id="95da6-111">0x000085A4</span></span>  <br/> |
|<span data-ttu-id="95da6-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="95da6-112">Data type:</span></span>  <br/> |<span data-ttu-id="95da6-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="95da6-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="95da6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="95da6-114">Area:</span></span>  <br/> |<span data-ttu-id="95da6-115">Task</span><span class="sxs-lookup"><span data-stu-id="95da6-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95da6-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95da6-116">Remarks</span></span>

<span data-ttu-id="95da6-117">Esta propiedad no se debe establecer en una tarea.</span><span class="sxs-lookup"><span data-stu-id="95da6-117">This property must not be set on a task.</span></span> <span data-ttu-id="95da6-118">Para indicar una propiedad vacía, no establezca esta propiedad en la cadena de longitud cero, pero en su lugar eliminarla.</span><span class="sxs-lookup"><span data-stu-id="95da6-118">To indicate an empty property, do not set this property to the zero-length string, but instead delete it.</span></span> 
  
<span data-ttu-id="95da6-119">Al marcar un objeto de mensaje y la propiedad no existe, un cliente debe escribir el valor de **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) a esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="95da6-119">When flagging a message object, and the property does not exist, a client should write the value of **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) to this property.</span></span>
  
<span data-ttu-id="95da6-120">En una lista de tareas pendientes consolidada, si esta propiedad no existe, un cliente debe sustituir el valor de la propiedad **PR_NORMALIZED_SUBJECT** al mostrar esta propiedad en la lista de tareas pendientes.</span><span class="sxs-lookup"><span data-stu-id="95da6-120">In a consolidated to-do list, if this property does not exist, a client should substitute the value of the **PR_NORMALIZED_SUBJECT** property when displaying this property in the to-do list.</span></span> 
  
<span data-ttu-id="95da6-121">En un objeto de mensaje de borrador, si el cliente implementa marcas de remitente, esta propiedad debe establecerse en el mismo valor que **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="95da6-121">On a draft message object, if the client implements sender flags, this property should be set to the same value as **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="95da6-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="95da6-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="95da6-123">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="95da6-123">Protocol specifications</span></span>

<span data-ttu-id="95da6-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95da6-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95da6-125">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas</span><span class="sxs-lookup"><span data-stu-id="95da6-125">Provides property set definitions and references to related Exchange Server protocol specifications</span></span>
    
<span data-ttu-id="95da6-126">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95da6-126">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95da6-127">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="95da6-127">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="95da6-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="95da6-128">Header files</span></span>

<span data-ttu-id="95da6-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95da6-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="95da6-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="95da6-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95da6-131">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="95da6-131">See also</span></span>



[<span data-ttu-id="95da6-132">Propiedad canónica PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="95da6-132">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
  
[<span data-ttu-id="95da6-133">Propiedad can�nico de PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="95da6-133">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)


[<span data-ttu-id="95da6-134">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="95da6-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="95da6-135">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="95da6-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="95da6-136">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="95da6-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="95da6-137">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="95da6-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

