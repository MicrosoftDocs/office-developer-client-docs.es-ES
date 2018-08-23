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
ms.openlocfilehash: 8c024f71279fac5dbb3d771442d9fbfb8a50e0f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578874"
---
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="9d16e-103">Propiedad canónica PidTagFormHostMap</span><span class="sxs-lookup"><span data-stu-id="9d16e-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="9d16e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d16e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d16e-105">Contiene un mapa de host de formularios disponibles.</span><span class="sxs-lookup"><span data-stu-id="9d16e-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d16e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9d16e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d16e-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="9d16e-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="9d16e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9d16e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9d16e-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="9d16e-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="9d16e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9d16e-110">Data type:</span></span>  <br/> |<span data-ttu-id="9d16e-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="9d16e-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="9d16e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9d16e-112">Area:</span></span>  <br/> |<span data-ttu-id="9d16e-113">MAPI comunes</span><span class="sxs-lookup"><span data-stu-id="9d16e-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d16e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9d16e-114">Remarks</span></span>

<span data-ttu-id="9d16e-115">Una aplicación de cliente debe actualizar esta propiedad, junto con la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), cuando se cambia la estructura subyacente en la interfaz de **IMAPIFormProp** .</span><span class="sxs-lookup"><span data-stu-id="9d16e-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9d16e-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9d16e-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9d16e-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9d16e-117">Header files</span></span>

<span data-ttu-id="9d16e-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d16e-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d16e-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9d16e-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="9d16e-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9d16e-120">Mapitags.h</span></span>
  
> <span data-ttu-id="9d16e-121">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="9d16e-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d16e-122">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="9d16e-122">See also</span></span>



[<span data-ttu-id="9d16e-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9d16e-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d16e-124">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="9d16e-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d16e-125">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9d16e-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d16e-126">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="9d16e-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

