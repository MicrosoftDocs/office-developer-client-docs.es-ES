---
title: Propiedad canónica PidTagCorrelate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelate
api_type:
- HeaderDef
ms.assetid: be34993e-ffcc-47f5-b2d4-95ffa707bc5c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ce8573310e17e26b4e2deb4c0a0f835a6569151e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819415"
---
# <a name="pidtagcorrelate-canonical-property"></a><span data-ttu-id="f8ebf-103">Propiedad canónica PidTagCorrelate</span><span class="sxs-lookup"><span data-stu-id="f8ebf-103">PidTagCorrelate Canonical Property</span></span>

  
  
<span data-ttu-id="f8ebf-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f8ebf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f8ebf-105">Contiene TRUE si el remitente de un mensaje solicita la característica de correlación del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="f8ebf-105">Contains TRUE if the sender of a message requests the correlation feature of the messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f8ebf-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f8ebf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f8ebf-107">PR_CORRELATE</span><span class="sxs-lookup"><span data-stu-id="f8ebf-107">PR_CORRELATE</span></span>  <br/> |
|<span data-ttu-id="f8ebf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f8ebf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f8ebf-109">0x0E0C</span><span class="sxs-lookup"><span data-stu-id="f8ebf-109">0x0E0C</span></span>  <br/> |
|<span data-ttu-id="f8ebf-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f8ebf-110">Data type:</span></span>  <br/> |<span data-ttu-id="f8ebf-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f8ebf-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f8ebf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f8ebf-112">Area:</span></span>  <br/> |<span data-ttu-id="f8ebf-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="f8ebf-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8ebf-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f8ebf-114">Remarks</span></span>

<span data-ttu-id="f8ebf-115">Esta propiedad se usa para solicitar la correlación de informes entrantes con el mensaje original enviado.</span><span class="sxs-lookup"><span data-stu-id="f8ebf-115">This property is used to request the correlation of incoming reports with the original sent message.</span></span> <span data-ttu-id="f8ebf-116">Cuando un proveedor de transporte encuentra un mensaje enviado con **PR_CORRELATE** establecido en TRUE, se establece la propiedad **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) para el identificador de sistema (MTS) de transferencia de mensaje para ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="f8ebf-116">When a transport provider encounters a submitted message with **PR_CORRELATE** set to TRUE, it sets the **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) property to the message transfer system (MTS) identifier for that message.</span></span>
  
 <span data-ttu-id="f8ebf-117">**PR_CORRELATE** debe utilizarse con sistemas de mensajería que admiten correlación por identificador de MTS, como X.400.</span><span class="sxs-lookup"><span data-stu-id="f8ebf-117">**PR_CORRELATE** should be used with messaging systems that support correlation by MTS identifier, such as X.400.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f8ebf-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f8ebf-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f8ebf-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f8ebf-119">Header files</span></span>

<span data-ttu-id="f8ebf-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f8ebf-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="f8ebf-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f8ebf-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="f8ebf-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f8ebf-122">Mapitags.h</span></span>
  
> <span data-ttu-id="f8ebf-123">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="f8ebf-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f8ebf-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8ebf-124">See also</span></span>



[<span data-ttu-id="f8ebf-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f8ebf-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f8ebf-126">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f8ebf-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f8ebf-127">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f8ebf-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f8ebf-128">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f8ebf-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

