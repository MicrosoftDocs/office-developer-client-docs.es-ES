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
ms.openlocfilehash: 68bb9a25131a07cf482a39cef70eb08a2b5a1756
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819818"
---
# <a name="pidtagoriginaldisplayto-canonical-property"></a><span data-ttu-id="27291-103">Propiedad canónica PidTagOriginalDisplayTo</span><span class="sxs-lookup"><span data-stu-id="27291-103">PidTagOriginalDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="27291-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27291-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27291-105">Contiene los nombres para mostrar de la principal (a) de los destinatarios del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="27291-105">Contains the display names of the primary (To) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27291-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="27291-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27291-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="27291-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="27291-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="27291-108">Identifier:</span></span>  <br/> |<span data-ttu-id="27291-109">0x0074</span><span class="sxs-lookup"><span data-stu-id="27291-109">0x0074</span></span>  <br/> |
|<span data-ttu-id="27291-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="27291-110">Data type:</span></span>  <br/> |<span data-ttu-id="27291-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="27291-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="27291-112">Área:</span><span class="sxs-lookup"><span data-stu-id="27291-112">Area:</span></span>  <br/> |<span data-ttu-id="27291-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="27291-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27291-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="27291-114">Remarks</span></span>

<span data-ttu-id="27291-115">Estas propiedades contienen una lista de ASCII separada por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="27291-115">These properties contain an ASCII list separated by semicolons.</span></span> <span data-ttu-id="27291-116">Que se proporciona mediante MAPI y se copia directamente desde **PR_DISPLAY_TO de MAPI** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) cuando una entrega o se ha generado el informe de no entrega o una lectura o informe nonread.</span><span class="sxs-lookup"><span data-stu-id="27291-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="27291-117">Esta propiedad puede estar presente en otros mensajes tal como se define por sus clases de mensaje.</span><span class="sxs-lookup"><span data-stu-id="27291-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="27291-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="27291-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="27291-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="27291-119">Protocol specifications</span></span>

<span data-ttu-id="27291-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27291-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27291-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="27291-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="27291-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27291-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27291-123">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="27291-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="27291-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="27291-124">Header files</span></span>

<span data-ttu-id="27291-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27291-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="27291-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="27291-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="27291-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="27291-127">Mapitags.h</span></span>
  
> <span data-ttu-id="27291-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="27291-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27291-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="27291-129">See also</span></span>



[<span data-ttu-id="27291-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="27291-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27291-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="27291-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27291-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="27291-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27291-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="27291-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

