---
title: Propiedad canónica PidTagOriginalDisplayCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayCc
api_type:
- COM
ms.assetid: f48d723c-3ad8-4617-952a-ba5216b2129c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9eb90d353705434803ff617ff2b355c7c96359b7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401534"
---
# <a name="pidtagoriginaldisplaycc-canonical-property"></a><span data-ttu-id="15b81-103">Propiedad canónica PidTagOriginalDisplayCc</span><span class="sxs-lookup"><span data-stu-id="15b81-103">PidTagOriginalDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="15b81-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15b81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15b81-105">Contiene los nombres para mostrar de los destinatarios con copia (CC) del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="15b81-105">Contains the display names of any carbon copy (CC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15b81-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="15b81-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15b81-107">PR_ORIGINAL_DISPLAY_CC, PR_ORIGINAL_DISPLAY_CC_A, PR_ORIGINAL_DISPLAY_CC_W</span><span class="sxs-lookup"><span data-stu-id="15b81-107">PR_ORIGINAL_DISPLAY_CC, PR_ORIGINAL_DISPLAY_CC_A, PR_ORIGINAL_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="15b81-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="15b81-108">Identifier:</span></span>  <br/> |<span data-ttu-id="15b81-109">0x0073</span><span class="sxs-lookup"><span data-stu-id="15b81-109">0x0073</span></span>  <br/> |
|<span data-ttu-id="15b81-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="15b81-110">Data type:</span></span>  <br/> |<span data-ttu-id="15b81-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="15b81-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="15b81-112">Área:</span><span class="sxs-lookup"><span data-stu-id="15b81-112">Area:</span></span>  <br/> |<span data-ttu-id="15b81-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="15b81-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15b81-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="15b81-114">Remarks</span></span>

<span data-ttu-id="15b81-115">Estas propiedades contienen una lista separada por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="15b81-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="15b81-116">Que se proporciona mediante MAPI y se copia directamente desde **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) cuando una entrega o se ha generado el informe de no entrega o una lectura o informe nonread.</span><span class="sxs-lookup"><span data-stu-id="15b81-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="15b81-117">Esta propiedad puede estar presente en otros mensajes tal como se define por sus clases de mensaje.</span><span class="sxs-lookup"><span data-stu-id="15b81-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="15b81-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="15b81-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="15b81-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="15b81-119">Protocol specifications</span></span>

<span data-ttu-id="15b81-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15b81-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15b81-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="15b81-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="15b81-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15b81-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15b81-123">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="15b81-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="15b81-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="15b81-124">Header files</span></span>

<span data-ttu-id="15b81-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15b81-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="15b81-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="15b81-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="15b81-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="15b81-127">Mapitags.h</span></span>
  
> <span data-ttu-id="15b81-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="15b81-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15b81-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="15b81-129">See also</span></span>



[<span data-ttu-id="15b81-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="15b81-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15b81-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="15b81-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15b81-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="15b81-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15b81-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="15b81-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

