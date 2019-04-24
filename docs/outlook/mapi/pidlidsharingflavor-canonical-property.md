---
title: Propiedad canónica PidLidSharingFlavor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingFlavor
api_type:
- COM
ms.assetid: c91ab5c7-82ac-4895-bf54-2863ca5e2410
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 21144af15e7a36f54af3032f735c391b3038305b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327485"
---
# <a name="pidlidsharingflavor-canonical-property"></a><span data-ttu-id="9ca35-103">Propiedad canónica PidLidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="9ca35-103">PidLidSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="9ca35-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ca35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ca35-105">Designa como una propiedad de un mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="9ca35-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ca35-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9ca35-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ca35-107">dispidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="9ca35-107">dispidSharingFlavor</span></span>  <br/> |
|<span data-ttu-id="9ca35-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="9ca35-108">Property set:</span></span>  <br/> |<span data-ttu-id="9ca35-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="9ca35-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="9ca35-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="9ca35-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9ca35-111">0x00008A18</span><span class="sxs-lookup"><span data-stu-id="9ca35-111">0x00008A18</span></span>  <br/> |
|<span data-ttu-id="9ca35-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9ca35-112">Data type:</span></span>  <br/> |<span data-ttu-id="9ca35-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9ca35-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9ca35-114">Área:</span><span class="sxs-lookup"><span data-stu-id="9ca35-114">Area:</span></span>  <br/> |<span data-ttu-id="9ca35-115">Uso compartido</span><span class="sxs-lookup"><span data-stu-id="9ca35-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ca35-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9ca35-116">Remarks</span></span>

<span data-ttu-id="9ca35-117">El valor de esta propiedad debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9ca35-117">The value of this property must be one of the following:</span></span>
  
|<span data-ttu-id="9ca35-118">**Value**</span><span class="sxs-lookup"><span data-stu-id="9ca35-118">**Value**</span></span>|<span data-ttu-id="9ca35-119">**Tipo de objeto de mensaje compartido**</span><span class="sxs-lookup"><span data-stu-id="9ca35-119">**Type of Sharing Message object**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9ca35-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="9ca35-120">0x00020310</span></span>  <br/> |<span data-ttu-id="9ca35-121">Una invitación para uso compartido de una carpeta especial.</span><span class="sxs-lookup"><span data-stu-id="9ca35-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="9ca35-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="9ca35-122">0x00000310</span></span>  <br/> |<span data-ttu-id="9ca35-123">Una invitación para uso compartido de una carpeta que no es una carpeta especial.</span><span class="sxs-lookup"><span data-stu-id="9ca35-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="9ca35-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="9ca35-124">0x00020500</span></span>  <br/> |<span data-ttu-id="9ca35-125">Una solicitud para compartir.</span><span class="sxs-lookup"><span data-stu-id="9ca35-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="9ca35-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="9ca35-126">0x00020710</span></span>  <br/> |<span data-ttu-id="9ca35-127">Una invitación para uso compartido de una carpeta especial y una solicitud de uso compartido para la carpeta especial equivalente del destinatario.</span><span class="sxs-lookup"><span data-stu-id="9ca35-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="9ca35-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="9ca35-128">0x00025100</span></span>  <br/> |<span data-ttu-id="9ca35-129">Respuesta para compartir que deniega una solicitud.</span><span class="sxs-lookup"><span data-stu-id="9ca35-129">A sharing response denying a request.</span></span>  <br/> |
|<span data-ttu-id="9ca35-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="9ca35-130">0x00023310</span></span>  <br/> |<span data-ttu-id="9ca35-131">Una respuesta para compartir que acepte una solicitud (también un tipo de invitación para compartir).</span><span class="sxs-lookup"><span data-stu-id="9ca35-131">A sharing response accepting a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9ca35-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ca35-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9ca35-133">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="9ca35-133">Protocol specifications</span></span>

<span data-ttu-id="9ca35-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ca35-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ca35-135">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9ca35-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9ca35-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ca35-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ca35-137">Comparte carpetas de buzones entre clientes.</span><span class="sxs-lookup"><span data-stu-id="9ca35-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9ca35-138">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9ca35-138">Header files</span></span>

<span data-ttu-id="9ca35-139">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9ca35-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ca35-140">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9ca35-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ca35-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ca35-141">See also</span></span>



[<span data-ttu-id="9ca35-142">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9ca35-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ca35-143">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="9ca35-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ca35-144">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9ca35-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ca35-145">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="9ca35-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

