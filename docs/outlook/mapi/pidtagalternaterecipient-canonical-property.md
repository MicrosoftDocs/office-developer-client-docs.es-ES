---
title: Propiedad canónica PidTagAlternateRecipient
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAlternateRecipient
api_type:
- HeaderDef
ms.assetid: df787b60-2f53-42ac-89b5-1b52c906f472
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ea78d9487e4929c2df3d49a9b85ba4aefac90a59
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819192"
---
# <a name="pidtagalternaterecipient-canonical-property"></a><span data-ttu-id="5a710-103">Propiedad canónica PidTagAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="5a710-103">PidTagAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="5a710-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a710-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a710-105">Contiene una lista de los identificadores de entrada para destinatarios alternativos designados por el destinatario original.</span><span class="sxs-lookup"><span data-stu-id="5a710-105">Contains a list of entry identifiers for alternate recipients designated by the original recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a710-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5a710-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a710-107">PR_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="5a710-107">PR_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="5a710-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5a710-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a710-109">0x3A01</span><span class="sxs-lookup"><span data-stu-id="5a710-109">0x3A01</span></span>  <br/> |
|<span data-ttu-id="5a710-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5a710-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a710-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5a710-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5a710-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5a710-112">Area:</span></span>  <br/> |<span data-ttu-id="5a710-113">Address</span><span class="sxs-lookup"><span data-stu-id="5a710-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a710-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5a710-114">Remarks</span></span>

<span data-ttu-id="5a710-115">Esta propiedad se usa para automático de los mensajes reenviado.</span><span class="sxs-lookup"><span data-stu-id="5a710-115">This property is used for auto forwarded messages.</span></span> <span data-ttu-id="5a710-116">Contiene una estructura [FLATENTRYLIST](flatentrylist.md) de destinatarios alternativos.</span><span class="sxs-lookup"><span data-stu-id="5a710-116">It contains a [FLATENTRYLIST](flatentrylist.md) structure of alternate recipients.</span></span> <span data-ttu-id="5a710-117">Si no se permite Autorreenvío o si no se ha designado ningún destinatario alternativo, se genera un informe de no entrega.</span><span class="sxs-lookup"><span data-stu-id="5a710-117">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5a710-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a710-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5a710-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5a710-119">Protocol specifications</span></span>

<span data-ttu-id="5a710-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a710-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a710-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5a710-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5a710-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a710-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a710-123">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="5a710-123">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="5a710-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a710-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a710-125">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="5a710-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="5a710-126">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a710-126">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a710-127">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="5a710-127">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5a710-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5a710-128">Header files</span></span>

<span data-ttu-id="5a710-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5a710-129">Mapitags.h</span></span>
  
> <span data-ttu-id="5a710-130">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="5a710-130">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="5a710-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a710-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a710-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5a710-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a710-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a710-133">See also</span></span>



[<span data-ttu-id="5a710-134">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="5a710-134">FLATENTRYLIST</span></span>](flatentrylist.md)


[<span data-ttu-id="5a710-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5a710-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a710-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5a710-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a710-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5a710-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a710-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5a710-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

