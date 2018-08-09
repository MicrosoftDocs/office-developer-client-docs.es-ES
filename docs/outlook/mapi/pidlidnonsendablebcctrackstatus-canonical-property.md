---
title: Propiedad canónica PidLidNonSendableBccTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableBccTrackStatus
api_type:
- COM
ms.assetid: daad8735-a3da-4a0b-9329-6eb253c281fd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da2bd4e87c7076872ccff708983cfbe631b27122
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818802"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a><span data-ttu-id="46c21-103">Propiedad canónica PidLidNonSendableBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="46c21-103">PidLidNonSendableBccTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="46c21-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="46c21-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="46c21-105">Contiene el valor para cada asistente que aparece en la propiedad **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="46c21-105">Contains the value for each attendee that is listed in the **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46c21-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="46c21-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="46c21-107">dispidNonSendBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="46c21-107">dispidNonSendBccTrackStatus</span></span>  <br/> |
|<span data-ttu-id="46c21-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="46c21-108">Property set:</span></span>  <br/> |<span data-ttu-id="46c21-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="46c21-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="46c21-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="46c21-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="46c21-111">0x00008545</span><span class="sxs-lookup"><span data-stu-id="46c21-111">0x00008545</span></span>  <br/> |
|<span data-ttu-id="46c21-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="46c21-112">Data type:</span></span>  <br/> |<span data-ttu-id="46c21-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="46c21-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="46c21-114">Área:</span><span class="sxs-lookup"><span data-stu-id="46c21-114">Area:</span></span>  <br/> |<span data-ttu-id="46c21-115">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="46c21-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46c21-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="46c21-116">Remarks</span></span>

<span data-ttu-id="46c21-117">Esta propiedad es necesaria sólo cuando se establece la propiedad **dispidNonSendableBCC** .</span><span class="sxs-lookup"><span data-stu-id="46c21-117">This property is required only when the **dispidNonSendableBCC** property is set.</span></span> <span data-ttu-id="46c21-118">El número de valores de esta propiedad debe ser igual que el número de valores en el **dispidNonSendableBCC**.</span><span class="sxs-lookup"><span data-stu-id="46c21-118">The number of values in this property must equal the number of values in the **dispidNonSendableBCC**.</span></span> <span data-ttu-id="46c21-119">Cada valor de esta propiedad se corresponde con el Asistente en la propiedad **dispidNonSendableBCC** en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="46c21-119">Each value in this property corresponds to the attendee in the **dispidNonSendableBCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="46c21-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="46c21-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="46c21-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="46c21-121">Protocol specifications</span></span>

<span data-ttu-id="46c21-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46c21-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46c21-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="46c21-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="46c21-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46c21-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46c21-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="46c21-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="46c21-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="46c21-126">Header files</span></span>

<span data-ttu-id="46c21-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="46c21-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="46c21-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="46c21-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46c21-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="46c21-129">See also</span></span>



[<span data-ttu-id="46c21-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="46c21-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="46c21-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="46c21-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="46c21-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="46c21-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="46c21-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="46c21-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

