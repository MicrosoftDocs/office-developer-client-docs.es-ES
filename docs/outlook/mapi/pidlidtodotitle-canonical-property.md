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
ms.openlocfilehash: 7ed69d9bab84a5c572026bb9480249c1212e3376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339945"
---
# <a name="pidlidtodotitle-canonical-property"></a><span data-ttu-id="33090-103">Propiedad canónica PidLidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="33090-103">PidLidToDoTitle Canonical Property</span></span>

  
  
<span data-ttu-id="33090-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33090-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33090-105">Contiene texto que puede ser especificado por el usuario para identificar este objeto de mensaje en una lista consolidada de tareas por hacer.</span><span class="sxs-lookup"><span data-stu-id="33090-105">Contains user-specifiable text to identify this message object in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33090-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="33090-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33090-107">dispidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="33090-107">dispidToDoTitle</span></span>  <br/> |
|<span data-ttu-id="33090-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="33090-108">Property set:</span></span>  <br/> |<span data-ttu-id="33090-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="33090-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="33090-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="33090-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="33090-111">0x000085A4</span><span class="sxs-lookup"><span data-stu-id="33090-111">0x000085A4</span></span>  <br/> |
|<span data-ttu-id="33090-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="33090-112">Data type:</span></span>  <br/> |<span data-ttu-id="33090-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="33090-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="33090-114">Área:</span><span class="sxs-lookup"><span data-stu-id="33090-114">Area:</span></span>  <br/> |<span data-ttu-id="33090-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="33090-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33090-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="33090-116">Remarks</span></span>

<span data-ttu-id="33090-117">Esta propiedad no debe establecerse en una tarea.</span><span class="sxs-lookup"><span data-stu-id="33090-117">This property must not be set on a task.</span></span> <span data-ttu-id="33090-118">Para indicar una propiedad vacía, no establezca esta propiedad en la cadena de longitud cero, sino que la elimine.</span><span class="sxs-lookup"><span data-stu-id="33090-118">To indicate an empty property, do not set this property to the zero-length string, but instead delete it.</span></span> 
  
<span data-ttu-id="33090-119">Al marcar un objeto message y la propiedad no existe, un cliente debe escribir el valor de **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="33090-119">When flagging a message object, and the property does not exist, a client should write the value of **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) to this property.</span></span>
  
<span data-ttu-id="33090-120">En una lista consolidada de tareas, si esta propiedad no existe, un cliente debe sustituir el valor de la propiedad **PR_NORMALIZED_SUBJECT** al mostrar esta propiedad en la lista de tareas por hacer.</span><span class="sxs-lookup"><span data-stu-id="33090-120">In a consolidated to-do list, if this property does not exist, a client should substitute the value of the **PR_NORMALIZED_SUBJECT** property when displaying this property in the to-do list.</span></span> 
  
<span data-ttu-id="33090-121">En un objeto de borrador de mensaje, si el cliente implementa marcas de remitente, esta propiedad debe establecerse en el mismo valor que **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="33090-121">On a draft message object, if the client implements sender flags, this property should be set to the same value as **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="33090-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="33090-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="33090-123">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="33090-123">Protocol specifications</span></span>

<span data-ttu-id="33090-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33090-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33090-125">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones Exchange Server de protocolo relacionados</span><span class="sxs-lookup"><span data-stu-id="33090-125">Provides property set definitions and references to related Exchange Server protocol specifications</span></span>
    
<span data-ttu-id="33090-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33090-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33090-127">Especifica las propiedades y las operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="33090-127">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="33090-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="33090-128">Header files</span></span>

<span data-ttu-id="33090-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="33090-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="33090-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="33090-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33090-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="33090-131">See also</span></span>



[<span data-ttu-id="33090-132">Propiedad canónica PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="33090-132">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
  
[<span data-ttu-id="33090-133">Propiedad can�nico de PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="33090-133">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)


[<span data-ttu-id="33090-134">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="33090-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33090-135">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="33090-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33090-136">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="33090-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33090-137">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="33090-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

