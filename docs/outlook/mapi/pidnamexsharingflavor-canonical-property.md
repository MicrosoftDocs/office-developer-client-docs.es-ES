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
ms.openlocfilehash: 1f07a11c47c6785bc9a166f11bde8f2e5ef464a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819140"
---
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="47d05-103">Propiedad canónica PidNameXSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="47d05-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="47d05-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="47d05-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="47d05-105">Representa el valor de la propiedad **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="47d05-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47d05-106">Nombres descriptivos:</span><span class="sxs-lookup"><span data-stu-id="47d05-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="47d05-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="47d05-107">None</span></span>  <br/> |
|<span data-ttu-id="47d05-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="47d05-108">Property set:</span></span>  <br/> |<span data-ttu-id="47d05-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="47d05-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="47d05-110">Nombre de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="47d05-110">Property name:</span></span>  <br/> |<span data-ttu-id="47d05-111">Tipo de uso compartido de X</span><span class="sxs-lookup"><span data-stu-id="47d05-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="47d05-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="47d05-112">Data type:</span></span>  <br/> |<span data-ttu-id="47d05-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="47d05-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="47d05-114">Área:</span><span class="sxs-lookup"><span data-stu-id="47d05-114">Area:</span></span>  <br/> |<span data-ttu-id="47d05-115">Uso compartido</span><span class="sxs-lookup"><span data-stu-id="47d05-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47d05-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="47d05-116">Remarks</span></span>

<span data-ttu-id="47d05-117">La propiedad **dispidSharingFlavor** debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="47d05-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="47d05-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="47d05-118">**Value**</span></span>|<span data-ttu-id="47d05-119">**Tipo de mensaje para compartir**</span><span class="sxs-lookup"><span data-stu-id="47d05-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="47d05-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="47d05-120">0x00020310</span></span>  <br/> |<span data-ttu-id="47d05-121">Una invitación para compartir de una carpeta especial.</span><span class="sxs-lookup"><span data-stu-id="47d05-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="47d05-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="47d05-122">0x00000310</span></span>  <br/> |<span data-ttu-id="47d05-123">Una invitación para compartir de una carpeta que no es una carpeta especial.</span><span class="sxs-lookup"><span data-stu-id="47d05-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="47d05-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="47d05-124">0x00020500</span></span>  <br/> |<span data-ttu-id="47d05-125">Una solicitud para compartir.</span><span class="sxs-lookup"><span data-stu-id="47d05-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="47d05-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="47d05-126">0x00020710</span></span>  <br/> |<span data-ttu-id="47d05-127">Ambos una invitación para compartir una carpeta especial y una solicitud para compartir para la carpeta del destinatario equivalente especiales.</span><span class="sxs-lookup"><span data-stu-id="47d05-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="47d05-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="47d05-128">0x00025100</span></span>  <br/> |<span data-ttu-id="47d05-129">Una respuesta para compartir que se deniega una solicitud.</span><span class="sxs-lookup"><span data-stu-id="47d05-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="47d05-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="47d05-130">0x00023310</span></span>  <br/> |<span data-ttu-id="47d05-131">Una respuesta para compartir que acepta una solicitud (también un tipo de invitación de uso compartido).</span><span class="sxs-lookup"><span data-stu-id="47d05-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="47d05-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="47d05-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="47d05-133">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="47d05-133">Protocol specifications</span></span>

<span data-ttu-id="47d05-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47d05-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47d05-135">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="47d05-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="47d05-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47d05-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47d05-137">Comparte las carpetas de buzón de correo entre los clientes.</span><span class="sxs-lookup"><span data-stu-id="47d05-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="47d05-138">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="47d05-138">Header files</span></span>

<span data-ttu-id="47d05-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47d05-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="47d05-140">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="47d05-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47d05-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="47d05-141">See also</span></span>



[<span data-ttu-id="47d05-142">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="47d05-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="47d05-143">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="47d05-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="47d05-144">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="47d05-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="47d05-145">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="47d05-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

