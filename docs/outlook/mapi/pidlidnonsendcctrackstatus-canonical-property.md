---
title: Propiedad canónica PidLidNonSendCcTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendCcTrackStatus
api_type:
- COM
ms.assetid: e2654fad-444b-45bc-976d-3c5cbbc81b84
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 10b6009bc86df4232c995e7c6bca463f45999528
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383180"
---
# <a name="pidlidnonsendcctrackstatus-canonical-property"></a><span data-ttu-id="6bda8-103">Propiedad canónica PidLidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="6bda8-103">PidLidNonSendCcTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="6bda8-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bda8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bda8-105">Contiene el valor para cada asistente que aparecen en la propiedad **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6bda8-105">Contains the value for each attendee listed in the **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6bda8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6bda8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6bda8-107">dispidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="6bda8-107">dispidNonSendCcTrackStatus</span></span>  <br/> |
|<span data-ttu-id="6bda8-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="6bda8-108">Property set:</span></span>  <br/> |<span data-ttu-id="6bda8-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="6bda8-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="6bda8-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="6bda8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6bda8-111">0x00008544</span><span class="sxs-lookup"><span data-stu-id="6bda8-111">0x00008544</span></span>  <br/> |
|<span data-ttu-id="6bda8-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6bda8-112">Data type:</span></span>  <br/> |<span data-ttu-id="6bda8-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="6bda8-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="6bda8-114">Área:</span><span class="sxs-lookup"><span data-stu-id="6bda8-114">Area:</span></span>  <br/> |<span data-ttu-id="6bda8-115">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="6bda8-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6bda8-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6bda8-116">Remarks</span></span>

<span data-ttu-id="6bda8-117">Esta propiedad es necesaria sólo cuando se establece la propiedad **dispidNonSendableCC** .</span><span class="sxs-lookup"><span data-stu-id="6bda8-117">This property is required only when the **dispidNonSendableCC** property is set.</span></span> <span data-ttu-id="6bda8-118">El número de valores de esta propiedad debe ser igual que el número de valores en **dispidNonSendableCC**.</span><span class="sxs-lookup"><span data-stu-id="6bda8-118">The number of values in this property must equal the number of values in **dispidNonSendableCC**.</span></span> <span data-ttu-id="6bda8-119">Cada valor PT_LONG en esta propiedad se corresponde con el Asistente en la propiedad **dispidNonSendableCC** en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="6bda8-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6bda8-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6bda8-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6bda8-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="6bda8-121">Protocol specifications</span></span>

<span data-ttu-id="6bda8-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6bda8-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6bda8-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6bda8-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6bda8-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6bda8-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6bda8-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="6bda8-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6bda8-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6bda8-126">Header files</span></span>

<span data-ttu-id="6bda8-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6bda8-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6bda8-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6bda8-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6bda8-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bda8-129">See also</span></span>



[<span data-ttu-id="6bda8-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6bda8-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6bda8-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="6bda8-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6bda8-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6bda8-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6bda8-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="6bda8-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

