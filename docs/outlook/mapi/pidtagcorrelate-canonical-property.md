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
ms.openlocfilehash: 063e41bf9fe306b3862e302abb4495ca56e3087b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575458"
---
# <a name="pidtagcorrelate-canonical-property"></a><span data-ttu-id="154f2-103">Propiedad canónica PidTagCorrelate</span><span class="sxs-lookup"><span data-stu-id="154f2-103">PidTagCorrelate Canonical Property</span></span>

  
  
<span data-ttu-id="154f2-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="154f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="154f2-105">Contiene TRUE si el remitente de un mensaje solicita la característica de correlación del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="154f2-105">Contains TRUE if the sender of a message requests the correlation feature of the messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="154f2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="154f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="154f2-107">PR_CORRELATE</span><span class="sxs-lookup"><span data-stu-id="154f2-107">PR_CORRELATE</span></span>  <br/> |
|<span data-ttu-id="154f2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="154f2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="154f2-109">0x0E0C</span><span class="sxs-lookup"><span data-stu-id="154f2-109">0x0E0C</span></span>  <br/> |
|<span data-ttu-id="154f2-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="154f2-110">Data type:</span></span>  <br/> |<span data-ttu-id="154f2-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="154f2-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="154f2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="154f2-112">Area:</span></span>  <br/> |<span data-ttu-id="154f2-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="154f2-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="154f2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="154f2-114">Remarks</span></span>

<span data-ttu-id="154f2-115">Esta propiedad se usa para solicitar la correlación de informes entrantes con el mensaje original enviado.</span><span class="sxs-lookup"><span data-stu-id="154f2-115">This property is used to request the correlation of incoming reports with the original sent message.</span></span> <span data-ttu-id="154f2-116">Cuando un proveedor de transporte encuentra un mensaje enviado con **PR_CORRELATE** establecido en TRUE, se establece la propiedad **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) para el identificador de sistema (MTS) de transferencia de mensaje para ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="154f2-116">When a transport provider encounters a submitted message with **PR_CORRELATE** set to TRUE, it sets the **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) property to the message transfer system (MTS) identifier for that message.</span></span>
  
 <span data-ttu-id="154f2-117">**PR_CORRELATE** debe utilizarse con sistemas de mensajería que admiten correlación por identificador de MTS, como X.400.</span><span class="sxs-lookup"><span data-stu-id="154f2-117">**PR_CORRELATE** should be used with messaging systems that support correlation by MTS identifier, such as X.400.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="154f2-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="154f2-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="154f2-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="154f2-119">Header files</span></span>

<span data-ttu-id="154f2-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="154f2-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="154f2-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="154f2-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="154f2-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="154f2-122">Mapitags.h</span></span>
  
> <span data-ttu-id="154f2-123">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="154f2-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="154f2-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="154f2-124">See also</span></span>



[<span data-ttu-id="154f2-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="154f2-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="154f2-126">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="154f2-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="154f2-127">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="154f2-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="154f2-128">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="154f2-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

