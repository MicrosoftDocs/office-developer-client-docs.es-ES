---
title: Propiedad canónica PidTagFormHostMap
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormHostMap
api_type:
- HeaderDef
ms.assetid: 92742747-cce0-4c54-9ece-1fcf652ac498
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 346776635fc36ffd8efd10cb232846831add20f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316229"
---
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="307a2-103">Propiedad canónica PidTagFormHostMap</span><span class="sxs-lookup"><span data-stu-id="307a2-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="307a2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="307a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="307a2-105">Contiene un mapa host de los formularios disponibles.</span><span class="sxs-lookup"><span data-stu-id="307a2-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="307a2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="307a2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="307a2-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="307a2-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="307a2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="307a2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="307a2-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="307a2-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="307a2-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="307a2-110">Data type:</span></span>  <br/> |<span data-ttu-id="307a2-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="307a2-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="307a2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="307a2-112">Area:</span></span>  <br/> |<span data-ttu-id="307a2-113">Common MAPI</span><span class="sxs-lookup"><span data-stu-id="307a2-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="307a2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="307a2-114">Remarks</span></span>

<span data-ttu-id="307a2-115">Una aplicación cliente debe actualizar esta propiedad, junto con la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), al cambiar la estructura subyacente en la interfaz **IMAPIFormProp** .</span><span class="sxs-lookup"><span data-stu-id="307a2-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="307a2-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="307a2-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="307a2-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="307a2-117">Header files</span></span>

<span data-ttu-id="307a2-118">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="307a2-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="307a2-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="307a2-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="307a2-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="307a2-120">Mapitags.h</span></span>
  
> <span data-ttu-id="307a2-121">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="307a2-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="307a2-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="307a2-122">See also</span></span>



[<span data-ttu-id="307a2-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="307a2-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="307a2-124">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="307a2-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="307a2-125">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="307a2-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="307a2-126">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="307a2-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

