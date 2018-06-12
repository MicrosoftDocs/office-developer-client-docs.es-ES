---
title: Propiedad canónico PidLidSharingFlavor
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 0333f0c309d89436c50a58124500f1b359584954
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818908"
---
# <a name="pidlidsharingflavor-canonical-property"></a><span data-ttu-id="1eb68-103">Propiedad canónico PidLidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="1eb68-103">PidLidSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="1eb68-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1eb68-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1eb68-105">Designa como una propiedad de un mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="1eb68-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1eb68-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1eb68-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1eb68-107">dispidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="1eb68-107">dispidSharingFlavor</span></span>  <br/> |
|<span data-ttu-id="1eb68-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="1eb68-108">Property set:</span></span>  <br/> |<span data-ttu-id="1eb68-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="1eb68-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="1eb68-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="1eb68-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1eb68-111">0x00008A18</span><span class="sxs-lookup"><span data-stu-id="1eb68-111">0x00008A18</span></span>  <br/> |
|<span data-ttu-id="1eb68-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1eb68-112">Data type:</span></span>  <br/> |<span data-ttu-id="1eb68-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1eb68-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1eb68-114">Área:</span><span class="sxs-lookup"><span data-stu-id="1eb68-114">Area:</span></span>  <br/> |<span data-ttu-id="1eb68-115">Uso compartido</span><span class="sxs-lookup"><span data-stu-id="1eb68-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1eb68-116">Notas</span><span class="sxs-lookup"><span data-stu-id="1eb68-116">Remarks</span></span>

<span data-ttu-id="1eb68-117">El valor de esta propiedad debe ser una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="1eb68-117">The value of this property must be one of the following:</span></span>
  
|<span data-ttu-id="1eb68-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1eb68-118">**Value**</span></span>|<span data-ttu-id="1eb68-119">**Tipo de objeto de mensaje de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="1eb68-119">**Type of Sharing Message object**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1eb68-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="1eb68-120">0x00020310</span></span>  <br/> |<span data-ttu-id="1eb68-121">Una invitación para compartir de una carpeta especial.</span><span class="sxs-lookup"><span data-stu-id="1eb68-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="1eb68-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="1eb68-122">0x00000310</span></span>  <br/> |<span data-ttu-id="1eb68-123">Una invitación para compartir de una carpeta que no es una carpeta especial.</span><span class="sxs-lookup"><span data-stu-id="1eb68-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="1eb68-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="1eb68-124">0x00020500</span></span>  <br/> |<span data-ttu-id="1eb68-125">Una solicitud para compartir.</span><span class="sxs-lookup"><span data-stu-id="1eb68-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="1eb68-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="1eb68-126">0x00020710</span></span>  <br/> |<span data-ttu-id="1eb68-127">Ambos una invitación para compartir una carpeta especial y una solicitud para compartir para la carpeta del destinatario equivalente especiales.</span><span class="sxs-lookup"><span data-stu-id="1eb68-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="1eb68-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="1eb68-128">0x00025100</span></span>  <br/> |<span data-ttu-id="1eb68-129">Una respuesta para compartir la denegación de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="1eb68-129">A sharing response denying a request.</span></span>  <br/> |
|<span data-ttu-id="1eb68-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="1eb68-130">0x00023310</span></span>  <br/> |<span data-ttu-id="1eb68-131">Una respuesta para compartir aceptación de una solicitud (también un tipo de invitación de uso compartido).</span><span class="sxs-lookup"><span data-stu-id="1eb68-131">A sharing response accepting a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1eb68-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1eb68-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1eb68-133">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1eb68-133">Protocol specifications</span></span>

<span data-ttu-id="1eb68-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1eb68-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1eb68-135">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1eb68-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1eb68-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1eb68-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1eb68-137">Comparte las carpetas de buzón de correo entre los clientes.</span><span class="sxs-lookup"><span data-stu-id="1eb68-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1eb68-138">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1eb68-138">Header files</span></span>

<span data-ttu-id="1eb68-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1eb68-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="1eb68-140">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1eb68-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1eb68-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="1eb68-141">See also</span></span>



[<span data-ttu-id="1eb68-142">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1eb68-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1eb68-143">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1eb68-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1eb68-144">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="1eb68-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1eb68-145">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="1eb68-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

