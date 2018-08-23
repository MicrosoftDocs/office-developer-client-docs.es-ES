---
title: Propiedad canónica PidTagAlternateRecipientAllowed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAlternateRecipientAllowed
api_type:
- HeaderDef
ms.assetid: dbbdeb54-3d14-4601-a77b-55ee31f33416
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0fcea0f0bc19140c5a0762143ce91bd41ea8fd07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569326"
---
# <a name="pidtagalternaterecipientallowed-canonical-property"></a><span data-ttu-id="b2605-103">Propiedad canónica PidTagAlternateRecipientAllowed</span><span class="sxs-lookup"><span data-stu-id="b2605-103">PidTagAlternateRecipientAllowed Canonical Property</span></span>

  
  
<span data-ttu-id="b2605-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2605-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2605-105">Contiene TRUE si el remitente lo permite el reenvío automático de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="b2605-105">Contains TRUE if the sender permits auto forwarding of this message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2605-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b2605-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b2605-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="b2605-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span></span>  <br/> |
|<span data-ttu-id="b2605-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b2605-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b2605-109">0x0002</span><span class="sxs-lookup"><span data-stu-id="b2605-109">0x0002</span></span>  <br/> |
|<span data-ttu-id="b2605-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b2605-110">Data type:</span></span>  <br/> |<span data-ttu-id="b2605-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b2605-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b2605-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b2605-112">Area:</span></span>  <br/> |<span data-ttu-id="b2605-113">Address</span><span class="sxs-lookup"><span data-stu-id="b2605-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2605-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b2605-114">Remarks</span></span>

<span data-ttu-id="b2605-115">Si no se permite el reenvío automático o si no se ha designado ningún destinatario alternativo, se debe generar un informe de no entrega.</span><span class="sxs-lookup"><span data-stu-id="b2605-115">If auto forwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b2605-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2605-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b2605-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="b2605-117">Protocol specifications</span></span>

<span data-ttu-id="b2605-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2605-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2605-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="b2605-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b2605-120">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2605-120">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2605-121">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="b2605-121">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="b2605-122">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2605-122">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2605-123">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="b2605-123">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="b2605-124">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2605-124">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2605-125">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="b2605-125">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b2605-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b2605-126">Header files</span></span>

<span data-ttu-id="b2605-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b2605-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b2605-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b2605-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="b2605-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b2605-129">Mapitags.h</span></span>
  
> <span data-ttu-id="b2605-130">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="b2605-130">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b2605-131">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="b2605-131">See also</span></span>



[<span data-ttu-id="b2605-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b2605-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b2605-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="b2605-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b2605-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b2605-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b2605-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="b2605-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

