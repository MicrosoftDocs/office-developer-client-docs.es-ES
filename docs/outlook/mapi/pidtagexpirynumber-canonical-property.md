---
title: Propiedad canónica PidTagExpiryNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryNumber
api_type:
- HeaderDef
ms.assetid: 644e8d3d-1792-4417-95a1-e978d0e6cd8e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 087585e936f04f18ad15f390a083213e2285da83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819485"
---
# <a name="pidtagexpirynumber-canonical-property"></a><span data-ttu-id="5c6fd-103">Propiedad canónica PidTagExpiryNumber</span><span class="sxs-lookup"><span data-stu-id="5c6fd-103">PidTagExpiryNumber Canonical Property</span></span>

  
  
<span data-ttu-id="5c6fd-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5c6fd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5c6fd-105">Define el tiempo de envío de caducidad junto con la propiedad **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5c6fd-105">Defines the expiry send time in conjunction with the **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5c6fd-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5c6fd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c6fd-107">PR_EXPIRY_NUMBER</span><span class="sxs-lookup"><span data-stu-id="5c6fd-107">PR_EXPIRY_NUMBER</span></span>  <br/> |
|<span data-ttu-id="5c6fd-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5c6fd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5c6fd-109">0x3FED</span><span class="sxs-lookup"><span data-stu-id="5c6fd-109">0x3FED</span></span>  <br/> |
|<span data-ttu-id="5c6fd-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5c6fd-110">Data type:</span></span>  <br/> |<span data-ttu-id="5c6fd-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5c6fd-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5c6fd-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5c6fd-112">Area:</span></span>  <br/> |<span data-ttu-id="5c6fd-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="5c6fd-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c6fd-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5c6fd-114">Remarks</span></span>

<span data-ttu-id="5c6fd-115">Valor de esta propiedad debe establecerse entre 0 y 999 ambos inclusive, si está presente.</span><span class="sxs-lookup"><span data-stu-id="5c6fd-115">This property's value must be set between 0 and 999 inclusive, if it is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5c6fd-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c6fd-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5c6fd-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5c6fd-117">Protocol specifications</span></span>

<span data-ttu-id="5c6fd-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c6fd-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c6fd-119">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5c6fd-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5c6fd-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5c6fd-120">Header files</span></span>

<span data-ttu-id="5c6fd-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c6fd-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c6fd-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5c6fd-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="5c6fd-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5c6fd-123">Mapitags.h</span></span>
  
> <span data-ttu-id="5c6fd-124">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="5c6fd-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c6fd-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c6fd-125">See also</span></span>



[<span data-ttu-id="5c6fd-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5c6fd-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5c6fd-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5c6fd-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5c6fd-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5c6fd-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5c6fd-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5c6fd-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

