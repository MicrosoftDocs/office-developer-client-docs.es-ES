---
title: Propiedad canónica PidNameXSharingFlavor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameXSharingFlavor
api_type:
- COM
ms.assetid: 7757fde1-564b-4f3a-9b9e-f80a143690ea
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d2afa598bf9b7949f2e9142611570ebbd048f7e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360889"
---
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="9ad4c-103">Propiedad canónica PidNameXSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="9ad4c-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="9ad4c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ad4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ad4c-105">Representa el valor de la propiedad **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9ad4c-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ad4c-106">Nombres descriptivos:</span><span class="sxs-lookup"><span data-stu-id="9ad4c-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="9ad4c-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9ad4c-107">None</span></span>  <br/> |
|<span data-ttu-id="9ad4c-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="9ad4c-108">Property set:</span></span>  <br/> |<span data-ttu-id="9ad4c-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="9ad4c-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="9ad4c-110">Nombre de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="9ad4c-110">Property name:</span></span>  <br/> |<span data-ttu-id="9ad4c-111">X-Sharing-Flavor</span><span class="sxs-lookup"><span data-stu-id="9ad4c-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="9ad4c-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9ad4c-112">Data type:</span></span>  <br/> |<span data-ttu-id="9ad4c-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9ad4c-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9ad4c-114">Área:</span><span class="sxs-lookup"><span data-stu-id="9ad4c-114">Area:</span></span>  <br/> |<span data-ttu-id="9ad4c-115">Uso compartido</span><span class="sxs-lookup"><span data-stu-id="9ad4c-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ad4c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9ad4c-116">Remarks</span></span>

<span data-ttu-id="9ad4c-117">La propiedad **dispidSharingFlavor** debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9ad4c-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="9ad4c-118">**Value**</span><span class="sxs-lookup"><span data-stu-id="9ad4c-118">**Value**</span></span>|<span data-ttu-id="9ad4c-119">**Tipo de mensaje para compartir**</span><span class="sxs-lookup"><span data-stu-id="9ad4c-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9ad4c-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="9ad4c-120">0x00020310</span></span>  <br/> |<span data-ttu-id="9ad4c-121">Una invitación para uso compartido de una carpeta especial.</span><span class="sxs-lookup"><span data-stu-id="9ad4c-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="9ad4c-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="9ad4c-122">0x00000310</span></span>  <br/> |<span data-ttu-id="9ad4c-123">Una invitación para uso compartido de una carpeta que no es una carpeta especial.</span><span class="sxs-lookup"><span data-stu-id="9ad4c-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="9ad4c-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="9ad4c-124">0x00020500</span></span>  <br/> |<span data-ttu-id="9ad4c-125">Una solicitud para compartir.</span><span class="sxs-lookup"><span data-stu-id="9ad4c-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="9ad4c-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="9ad4c-126">0x00020710</span></span>  <br/> |<span data-ttu-id="9ad4c-127">Una invitación para uso compartido de una carpeta especial y una solicitud de uso compartido para la carpeta especial equivalente del destinatario.</span><span class="sxs-lookup"><span data-stu-id="9ad4c-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="9ad4c-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="9ad4c-128">0x00025100</span></span>  <br/> |<span data-ttu-id="9ad4c-129">Una respuesta para compartir que deniega una solicitud.</span><span class="sxs-lookup"><span data-stu-id="9ad4c-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="9ad4c-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="9ad4c-130">0x00023310</span></span>  <br/> |<span data-ttu-id="9ad4c-131">Una respuesta para compartir que acepta una solicitud (también un tipo de invitación para compartir).</span><span class="sxs-lookup"><span data-stu-id="9ad4c-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9ad4c-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ad4c-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9ad4c-133">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="9ad4c-133">Protocol specifications</span></span>

<span data-ttu-id="9ad4c-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ad4c-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ad4c-135">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9ad4c-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9ad4c-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ad4c-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ad4c-137">Comparte carpetas de buzones entre clientes.</span><span class="sxs-lookup"><span data-stu-id="9ad4c-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9ad4c-138">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9ad4c-138">Header files</span></span>

<span data-ttu-id="9ad4c-139">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9ad4c-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ad4c-140">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9ad4c-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ad4c-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ad4c-141">See also</span></span>



[<span data-ttu-id="9ad4c-142">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9ad4c-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ad4c-143">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="9ad4c-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ad4c-144">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9ad4c-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ad4c-145">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="9ad4c-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

