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
ms.openlocfilehash: 7c304de3184e49044d3f83cef1f1ebaac019b2ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360100"
---
# <a name="pidtagalternaterecipient-canonical-property"></a><span data-ttu-id="e538d-103">Propiedad canónica PidTagAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="e538d-103">PidTagAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="e538d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e538d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e538d-105">Contiene una lista de identificadores de entrada para destinatarios alternativos designados por el destinatario original.</span><span class="sxs-lookup"><span data-stu-id="e538d-105">Contains a list of entry identifiers for alternate recipients designated by the original recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e538d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e538d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e538d-107">PR_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="e538d-107">PR_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="e538d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e538d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e538d-109">0x3A01</span><span class="sxs-lookup"><span data-stu-id="e538d-109">0x3A01</span></span>  <br/> |
|<span data-ttu-id="e538d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e538d-110">Data type:</span></span>  <br/> |<span data-ttu-id="e538d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e538d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e538d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e538d-112">Area:</span></span>  <br/> |<span data-ttu-id="e538d-113">Dirección</span><span class="sxs-lookup"><span data-stu-id="e538d-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e538d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e538d-114">Remarks</span></span>

<span data-ttu-id="e538d-115">Esta propiedad se usa para los mensajes reenviados automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e538d-115">This property is used for auto forwarded messages.</span></span> <span data-ttu-id="e538d-116">Contiene una estructura [FLATENTRYLIST](flatentrylist.md) de destinatarios alternativos.</span><span class="sxs-lookup"><span data-stu-id="e538d-116">It contains a [FLATENTRYLIST](flatentrylist.md) structure of alternate recipients.</span></span> <span data-ttu-id="e538d-117">Si no se permite el autoforwarding o si no se ha designado ningún destinatario alternativo, se genera un informe de no entrega.</span><span class="sxs-lookup"><span data-stu-id="e538d-117">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e538d-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e538d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e538d-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="e538d-119">Protocol specifications</span></span>

<span data-ttu-id="e538d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e538d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e538d-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="e538d-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e538d-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e538d-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e538d-123">Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="e538d-123">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e538d-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e538d-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e538d-125">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="e538d-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="e538d-126">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e538d-126">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e538d-127">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficiente.</span><span class="sxs-lookup"><span data-stu-id="e538d-127">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e538d-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e538d-128">Header files</span></span>

<span data-ttu-id="e538d-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e538d-129">Mapitags.h</span></span>
  
> <span data-ttu-id="e538d-130">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="e538d-130">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="e538d-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e538d-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="e538d-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e538d-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e538d-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="e538d-133">See also</span></span>



[<span data-ttu-id="e538d-134">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="e538d-134">FLATENTRYLIST</span></span>](flatentrylist.md)


[<span data-ttu-id="e538d-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e538d-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e538d-136">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e538d-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e538d-137">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e538d-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e538d-138">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="e538d-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

