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
ms.openlocfilehash: 9e0316ead2adf00619bd87c57946ba72ed01f4b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819547"
---
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="021f7-103">Propiedad canónica PidTagFormHostMap</span><span class="sxs-lookup"><span data-stu-id="021f7-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="021f7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="021f7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="021f7-105">Contiene un mapa de host de formularios disponibles.</span><span class="sxs-lookup"><span data-stu-id="021f7-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="021f7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="021f7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="021f7-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="021f7-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="021f7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="021f7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="021f7-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="021f7-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="021f7-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="021f7-110">Data type:</span></span>  <br/> |<span data-ttu-id="021f7-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="021f7-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="021f7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="021f7-112">Area:</span></span>  <br/> |<span data-ttu-id="021f7-113">MAPI comunes</span><span class="sxs-lookup"><span data-stu-id="021f7-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="021f7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="021f7-114">Remarks</span></span>

<span data-ttu-id="021f7-115">Una aplicación de cliente debe actualizar esta propiedad, junto con la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), cuando se cambia la estructura subyacente en la interfaz de **IMAPIFormProp** .</span><span class="sxs-lookup"><span data-stu-id="021f7-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="021f7-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="021f7-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="021f7-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="021f7-117">Header files</span></span>

<span data-ttu-id="021f7-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="021f7-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="021f7-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="021f7-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="021f7-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="021f7-120">Mapitags.h</span></span>
  
> <span data-ttu-id="021f7-121">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="021f7-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="021f7-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="021f7-122">See also</span></span>



[<span data-ttu-id="021f7-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="021f7-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="021f7-124">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="021f7-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="021f7-125">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="021f7-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="021f7-126">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="021f7-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

