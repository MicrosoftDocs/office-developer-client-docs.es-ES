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
ms.openlocfilehash: dc77f9c7b58fc925048d6dec2bee2ff96a8723b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819201"
---
# <a name="pidtagalternaterecipientallowed-canonical-property"></a><span data-ttu-id="12c2b-103">Propiedad canónica PidTagAlternateRecipientAllowed</span><span class="sxs-lookup"><span data-stu-id="12c2b-103">PidTagAlternateRecipientAllowed Canonical Property</span></span>

  
  
<span data-ttu-id="12c2b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="12c2b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="12c2b-105">Contiene TRUE si el remitente lo permite el reenvío automático de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="12c2b-105">Contains TRUE if the sender permits auto forwarding of this message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="12c2b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="12c2b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="12c2b-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="12c2b-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span></span>  <br/> |
|<span data-ttu-id="12c2b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="12c2b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="12c2b-109">0x0002</span><span class="sxs-lookup"><span data-stu-id="12c2b-109">0x0002</span></span>  <br/> |
|<span data-ttu-id="12c2b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="12c2b-110">Data type:</span></span>  <br/> |<span data-ttu-id="12c2b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="12c2b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="12c2b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="12c2b-112">Area:</span></span>  <br/> |<span data-ttu-id="12c2b-113">Address</span><span class="sxs-lookup"><span data-stu-id="12c2b-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12c2b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="12c2b-114">Remarks</span></span>

<span data-ttu-id="12c2b-115">Si no se permite el reenvío automático o si no se ha designado ningún destinatario alternativo, se debe generar un informe de no entrega.</span><span class="sxs-lookup"><span data-stu-id="12c2b-115">If auto forwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="12c2b-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="12c2b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="12c2b-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="12c2b-117">Protocol specifications</span></span>

<span data-ttu-id="12c2b-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12c2b-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12c2b-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="12c2b-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="12c2b-120">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12c2b-120">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12c2b-121">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="12c2b-121">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="12c2b-122">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12c2b-122">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12c2b-123">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="12c2b-123">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="12c2b-124">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12c2b-124">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12c2b-125">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="12c2b-125">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="12c2b-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="12c2b-126">Header files</span></span>

<span data-ttu-id="12c2b-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="12c2b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="12c2b-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="12c2b-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="12c2b-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="12c2b-129">Mapitags.h</span></span>
  
> <span data-ttu-id="12c2b-130">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="12c2b-130">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12c2b-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="12c2b-131">See also</span></span>



[<span data-ttu-id="12c2b-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="12c2b-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="12c2b-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="12c2b-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="12c2b-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="12c2b-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="12c2b-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="12c2b-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

