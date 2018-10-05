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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396718"
---
# <a name="pidtagoriginaldisplaybcc-canonical-property"></a><span data-ttu-id="7da47-103">Propiedad canónica PidTagOriginalDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="7da47-103">PidTagOriginalDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="7da47-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7da47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7da47-105">Contiene los nombres para mostrar de los destinatarios de copia carbón (oculta CCO) del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="7da47-105">Contains the display names of any blind carbon copy (BCC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7da47-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7da47-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7da47-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="7da47-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="7da47-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7da47-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7da47-109">0x0072</span><span class="sxs-lookup"><span data-stu-id="7da47-109">0x0072</span></span>  <br/> |
|<span data-ttu-id="7da47-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7da47-110">Data type:</span></span>  <br/> |<span data-ttu-id="7da47-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7da47-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7da47-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7da47-112">Area:</span></span>  <br/> |<span data-ttu-id="7da47-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="7da47-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7da47-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7da47-114">Remarks</span></span>

<span data-ttu-id="7da47-115">Estas propiedades contienen una lista separada por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="7da47-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="7da47-116">Que se proporciona mediante MAPI y se copian directamente desde **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) cuando se genera una entrega o informe de no entrega o una lectura o informe nonread.</span><span class="sxs-lookup"><span data-stu-id="7da47-116">They is furnished by MAPI and are copied directly from **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="7da47-117">Estas propiedades pueden estar presentes en otros mensajes tal como se define por sus clases de mensaje.</span><span class="sxs-lookup"><span data-stu-id="7da47-117">These properties may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7da47-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7da47-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7da47-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="7da47-119">Protocol specifications</span></span>

<span data-ttu-id="7da47-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7da47-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7da47-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7da47-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7da47-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7da47-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7da47-123">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="7da47-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7da47-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7da47-124">Header files</span></span>

<span data-ttu-id="7da47-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7da47-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="7da47-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7da47-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="7da47-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7da47-127">Mapitags.h</span></span>
  
> <span data-ttu-id="7da47-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7da47-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7da47-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7da47-129">See also</span></span>



[<span data-ttu-id="7da47-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7da47-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7da47-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="7da47-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7da47-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7da47-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7da47-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="7da47-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

