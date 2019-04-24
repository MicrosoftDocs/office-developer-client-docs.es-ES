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
# <a name="pidlidtodotitle-canonical-property"></a><span data-ttu-id="40094-103">Propiedad canónica PidLidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="40094-103">PidLidToDoTitle Canonical Property</span></span>

  
  
<span data-ttu-id="40094-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40094-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40094-105">Contiene texto especificable por el usuario para identificar este objeto de mensaje en una lista de tareas pendientes consolidada.</span><span class="sxs-lookup"><span data-stu-id="40094-105">Contains user-specifiable text to identify this message object in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40094-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="40094-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="40094-107">dispidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="40094-107">dispidToDoTitle</span></span>  <br/> |
|<span data-ttu-id="40094-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="40094-108">Property set:</span></span>  <br/> |<span data-ttu-id="40094-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="40094-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="40094-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="40094-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="40094-111">0x000085A4</span><span class="sxs-lookup"><span data-stu-id="40094-111">0x000085A4</span></span>  <br/> |
|<span data-ttu-id="40094-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="40094-112">Data type:</span></span>  <br/> |<span data-ttu-id="40094-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="40094-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="40094-114">Área:</span><span class="sxs-lookup"><span data-stu-id="40094-114">Area:</span></span>  <br/> |<span data-ttu-id="40094-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="40094-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40094-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="40094-116">Remarks</span></span>

<span data-ttu-id="40094-117">Esta propiedad no se debe establecer en una tarea.</span><span class="sxs-lookup"><span data-stu-id="40094-117">This property must not be set on a task.</span></span> <span data-ttu-id="40094-118">Para indicar una propiedad vacía, no establezca esta propiedad en la cadena de longitud cero, pero elimínela en su lugar.</span><span class="sxs-lookup"><span data-stu-id="40094-118">To indicate an empty property, do not set this property to the zero-length string, but instead delete it.</span></span> 
  
<span data-ttu-id="40094-119">Al marcar un objeto de mensaje y la propiedad no existe, un cliente debe escribir el valor de **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="40094-119">When flagging a message object, and the property does not exist, a client should write the value of **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) to this property.</span></span>
  
<span data-ttu-id="40094-120">En una lista de tareas pendientes consolidada, si esta propiedad no existe, un cliente debe sustituir el valor de la propiedad **PR_NORMALIZED_SUBJECT** al mostrar esta propiedad en la lista de tareas pendientes.</span><span class="sxs-lookup"><span data-stu-id="40094-120">In a consolidated to-do list, if this property does not exist, a client should substitute the value of the **PR_NORMALIZED_SUBJECT** property when displaying this property in the to-do list.</span></span> 
  
<span data-ttu-id="40094-121">En un objeto de mensaje de borrador, si el cliente implementa marcas de remitente, esta propiedad debe establecerse en el mismo valor que **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="40094-121">On a draft message object, if the client implements sender flags, this property should be set to the same value as **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="40094-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="40094-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="40094-123">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="40094-123">Protocol specifications</span></span>

<span data-ttu-id="40094-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40094-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40094-125">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas</span><span class="sxs-lookup"><span data-stu-id="40094-125">Provides property set definitions and references to related Exchange Server protocol specifications</span></span>
    
<span data-ttu-id="40094-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40094-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40094-127">Especifica las propiedades y operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="40094-127">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="40094-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="40094-128">Header files</span></span>

<span data-ttu-id="40094-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="40094-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="40094-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="40094-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="40094-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="40094-131">See also</span></span>



[<span data-ttu-id="40094-132">Propiedad canónica PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="40094-132">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
  
[<span data-ttu-id="40094-133">Propiedad can�nico de PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="40094-133">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)


[<span data-ttu-id="40094-134">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="40094-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="40094-135">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="40094-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="40094-136">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="40094-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="40094-137">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="40094-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

