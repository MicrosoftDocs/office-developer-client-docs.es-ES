---
title: Propiedad canónica PidTagOriginalDisplayBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayBcc
api_type:
- COM
ms.assetid: 7bf66f0c-3095-4b4a-a32e-db278e1adc5a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3fbd7205901616695bcdcd012601afd252ac05f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355646"
---
# <a name="pidtagoriginaldisplaybcc-canonical-property"></a><span data-ttu-id="07214-103">Propiedad canónica PidTagOriginalDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="07214-103">PidTagOriginalDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="07214-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07214-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07214-105">Contiene los nombres para mostrar de cualquier destinatario de copia oculta (CCO) del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="07214-105">Contains the display names of any blind carbon copy (BCC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="07214-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="07214-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="07214-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="07214-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="07214-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="07214-108">Identifier:</span></span>  <br/> |<span data-ttu-id="07214-109">0x0072</span><span class="sxs-lookup"><span data-stu-id="07214-109">0x0072</span></span>  <br/> |
|<span data-ttu-id="07214-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="07214-110">Data type:</span></span>  <br/> |<span data-ttu-id="07214-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="07214-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="07214-112">Área:</span><span class="sxs-lookup"><span data-stu-id="07214-112">Area:</span></span>  <br/> |<span data-ttu-id="07214-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="07214-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07214-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="07214-114">Remarks</span></span>

<span data-ttu-id="07214-115">Estas propiedades contienen una lista separada por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="07214-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="07214-116">Se entregan mediante MAPI y se copian directamente desde **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) cuando se genera un informe de entrega o no entrega o un informe de lectura o no leído.</span><span class="sxs-lookup"><span data-stu-id="07214-116">They is furnished by MAPI and are copied directly from **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="07214-117">Estas propiedades pueden estar presentes en otros mensajes definidos por sus clases de mensaje.</span><span class="sxs-lookup"><span data-stu-id="07214-117">These properties may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="07214-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="07214-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="07214-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="07214-119">Protocol specifications</span></span>

<span data-ttu-id="07214-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07214-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07214-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="07214-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="07214-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07214-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07214-123">Especifica las propiedades y las operaciones permitidas en objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="07214-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="07214-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="07214-124">Header files</span></span>

<span data-ttu-id="07214-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="07214-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="07214-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="07214-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="07214-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="07214-127">Mapitags.h</span></span>
  
> <span data-ttu-id="07214-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="07214-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="07214-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="07214-129">See also</span></span>



[<span data-ttu-id="07214-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="07214-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="07214-131">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="07214-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="07214-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="07214-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="07214-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="07214-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

