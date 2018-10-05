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
ms.openlocfilehash: e5c795f15046bcab40abc2396b36e14925d3869d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386946"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a><span data-ttu-id="7d3cc-103">Propiedad canónica PidLidNonSendableBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="7d3cc-103">PidLidNonSendableBccTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="7d3cc-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d3cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d3cc-105">Contiene el valor para cada asistente que aparece en la propiedad **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7d3cc-105">Contains the value for each attendee that is listed in the **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7d3cc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7d3cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d3cc-107">dispidNonSendBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="7d3cc-107">dispidNonSendBccTrackStatus</span></span>  <br/> |
|<span data-ttu-id="7d3cc-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="7d3cc-108">Property set:</span></span>  <br/> |<span data-ttu-id="7d3cc-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="7d3cc-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="7d3cc-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="7d3cc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7d3cc-111">0x00008545</span><span class="sxs-lookup"><span data-stu-id="7d3cc-111">0x00008545</span></span>  <br/> |
|<span data-ttu-id="7d3cc-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7d3cc-112">Data type:</span></span>  <br/> |<span data-ttu-id="7d3cc-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="7d3cc-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="7d3cc-114">Área:</span><span class="sxs-lookup"><span data-stu-id="7d3cc-114">Area:</span></span>  <br/> |<span data-ttu-id="7d3cc-115">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="7d3cc-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d3cc-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7d3cc-116">Remarks</span></span>

<span data-ttu-id="7d3cc-117">Esta propiedad es necesaria sólo cuando se establece la propiedad **dispidNonSendableBCC** .</span><span class="sxs-lookup"><span data-stu-id="7d3cc-117">This property is required only when the **dispidNonSendableBCC** property is set.</span></span> <span data-ttu-id="7d3cc-118">El número de valores de esta propiedad debe ser igual que el número de valores en el **dispidNonSendableBCC**.</span><span class="sxs-lookup"><span data-stu-id="7d3cc-118">The number of values in this property must equal the number of values in the **dispidNonSendableBCC**.</span></span> <span data-ttu-id="7d3cc-119">Cada valor de esta propiedad se corresponde con el Asistente en la propiedad **dispidNonSendableBCC** en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="7d3cc-119">Each value in this property corresponds to the attendee in the **dispidNonSendableBCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7d3cc-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d3cc-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7d3cc-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="7d3cc-121">Protocol specifications</span></span>

<span data-ttu-id="7d3cc-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d3cc-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d3cc-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7d3cc-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7d3cc-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d3cc-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d3cc-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="7d3cc-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7d3cc-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7d3cc-126">Header files</span></span>

<span data-ttu-id="7d3cc-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d3cc-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d3cc-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7d3cc-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d3cc-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d3cc-129">See also</span></span>



[<span data-ttu-id="7d3cc-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7d3cc-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d3cc-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="7d3cc-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d3cc-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7d3cc-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d3cc-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="7d3cc-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

