---
title: Propiedad canónica PidTagOriginalDisplayTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayTo
api_type:
- COM
ms.assetid: 8c1cf14c-0339-4ced-8f68-4bfaa1e4d3e9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5a2f60051e5cb0717926a5c3e2f878a49919b04c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342704"
---
# <a name="pidtagoriginaldisplayto-canonical-property"></a><span data-ttu-id="b10d7-103">Propiedad canónica PidTagOriginalDisplayTo</span><span class="sxs-lookup"><span data-stu-id="b10d7-103">PidTagOriginalDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="b10d7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b10d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b10d7-105">Contiene los nombres para mostrar de los destinatarios principales (Para) del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="b10d7-105">Contains the display names of the primary (To) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b10d7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b10d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b10d7-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="b10d7-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="b10d7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b10d7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b10d7-109">0x0074</span><span class="sxs-lookup"><span data-stu-id="b10d7-109">0x0074</span></span>  <br/> |
|<span data-ttu-id="b10d7-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b10d7-110">Data type:</span></span>  <br/> |<span data-ttu-id="b10d7-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b10d7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b10d7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b10d7-112">Area:</span></span>  <br/> |<span data-ttu-id="b10d7-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="b10d7-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b10d7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b10d7-114">Remarks</span></span>

<span data-ttu-id="b10d7-115">Estas propiedades contienen una lista ASCII separada por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="b10d7-115">These properties contain an ASCII list separated by semicolons.</span></span> <span data-ttu-id="b10d7-116">Se entrega mediante MAPI y se copia directamente desde **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) cuando se genera un informe de entrega o no entrega o un informe leído o no leído.</span><span class="sxs-lookup"><span data-stu-id="b10d7-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="b10d7-117">Esta propiedad puede estar presente en otros mensajes definidos por sus clases de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b10d7-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b10d7-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b10d7-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b10d7-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="b10d7-119">Protocol specifications</span></span>

<span data-ttu-id="b10d7-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b10d7-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b10d7-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="b10d7-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b10d7-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b10d7-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b10d7-123">Especifica las propiedades y operaciones permitidas en los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b10d7-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b10d7-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b10d7-124">Header files</span></span>

<span data-ttu-id="b10d7-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b10d7-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="b10d7-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b10d7-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="b10d7-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b10d7-127">Mapitags.h</span></span>
  
> <span data-ttu-id="b10d7-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="b10d7-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b10d7-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b10d7-129">See also</span></span>



[<span data-ttu-id="b10d7-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b10d7-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b10d7-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="b10d7-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b10d7-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b10d7-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b10d7-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="b10d7-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

