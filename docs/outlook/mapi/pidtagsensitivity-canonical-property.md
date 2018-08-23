---
title: Propiedad canónica PidTagSensitivity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSensitivity
api_type:
- COM
ms.assetid: 5b678475-f2a8-4831-ad68-11654e09c821
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f30a5848e07de03e61d3a63188aa7b608504ff24
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573736"
---
# <a name="pidtagsensitivity-canonical-property"></a><span data-ttu-id="63fd6-103">Propiedad canónica PidTagSensitivity</span><span class="sxs-lookup"><span data-stu-id="63fd6-103">PidTagSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="63fd6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63fd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63fd6-105">Contiene un valor que indica la opinión de la dirección del remitente del mensaje de la confidencialidad de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="63fd6-105">Contains a value that indicates the message sender's opinion of the sensitivity of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="63fd6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="63fd6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="63fd6-107">PR_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="63fd6-107">PR_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="63fd6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="63fd6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="63fd6-109">0x0036</span><span class="sxs-lookup"><span data-stu-id="63fd6-109">0x0036</span></span>  <br/> |
|<span data-ttu-id="63fd6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="63fd6-110">Data type:</span></span>  <br/> |<span data-ttu-id="63fd6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="63fd6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="63fd6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="63fd6-112">Area:</span></span>  <br/> |<span data-ttu-id="63fd6-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="63fd6-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63fd6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63fd6-114">Remarks</span></span>

<span data-ttu-id="63fd6-115">Se recomienda que los objetos de mensaje exponen esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="63fd6-115">It is recommended that message objects expose this property.</span></span>
  
<span data-ttu-id="63fd6-116">Esta propiedad puede tener exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="63fd6-116">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="63fd6-117">SENSITIVITY_NONE</span><span class="sxs-lookup"><span data-stu-id="63fd6-117">SENSITIVITY_NONE</span></span> 
  
> <span data-ttu-id="63fd6-118">El mensaje no tiene sensibilidad especial.</span><span class="sxs-lookup"><span data-stu-id="63fd6-118">The message has no special sensitivity.</span></span>
    
<span data-ttu-id="63fd6-119">SENSITIVITY_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="63fd6-119">SENSITIVITY_PERSONAL</span></span> 
  
> <span data-ttu-id="63fd6-120">El mensaje es personal.</span><span class="sxs-lookup"><span data-stu-id="63fd6-120">The message is personal.</span></span>
    
<span data-ttu-id="63fd6-121">SENSITIVITY_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="63fd6-121">SENSITIVITY_PRIVATE</span></span> 
  
> <span data-ttu-id="63fd6-122">El mensaje es privado.</span><span class="sxs-lookup"><span data-stu-id="63fd6-122">The message is private.</span></span>
    
<span data-ttu-id="63fd6-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span><span class="sxs-lookup"><span data-stu-id="63fd6-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span></span> 
  
> <span data-ttu-id="63fd6-124">El mensaje se designa confidencial de la empresa.</span><span class="sxs-lookup"><span data-stu-id="63fd6-124">The message is designated company confidential.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="63fd6-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="63fd6-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="63fd6-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="63fd6-126">Protocol specifications</span></span>

<span data-ttu-id="63fd6-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63fd6-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63fd6-128">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="63fd6-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="63fd6-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63fd6-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63fd6-130">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="63fd6-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="63fd6-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="63fd6-131">Header files</span></span>

<span data-ttu-id="63fd6-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="63fd6-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="63fd6-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="63fd6-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="63fd6-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="63fd6-134">Mapitags.h</span></span>
  
> <span data-ttu-id="63fd6-135">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="63fd6-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63fd6-136">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="63fd6-136">See also</span></span>



[<span data-ttu-id="63fd6-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="63fd6-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63fd6-138">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="63fd6-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63fd6-139">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="63fd6-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63fd6-140">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="63fd6-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

