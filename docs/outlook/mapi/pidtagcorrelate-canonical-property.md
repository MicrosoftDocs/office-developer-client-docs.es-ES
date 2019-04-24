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
ms.openlocfilehash: ea217808a163c7f16bbaa3c5a959fd32c8cbe10c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357921"
---
# <a name="pidtagcorrelate-canonical-property"></a><span data-ttu-id="cb684-103">Propiedad canónica PidTagCorrelate</span><span class="sxs-lookup"><span data-stu-id="cb684-103">PidTagCorrelate Canonical Property</span></span>

  
  
<span data-ttu-id="cb684-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb684-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb684-105">Contiene TRUE si el remitente de un mensaje solicita la característica de correlación del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="cb684-105">Contains TRUE if the sender of a message requests the correlation feature of the messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cb684-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cb684-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb684-107">PR_CORRELATE</span><span class="sxs-lookup"><span data-stu-id="cb684-107">PR_CORRELATE</span></span>  <br/> |
|<span data-ttu-id="cb684-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cb684-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cb684-109">0x0E0C</span><span class="sxs-lookup"><span data-stu-id="cb684-109">0x0E0C</span></span>  <br/> |
|<span data-ttu-id="cb684-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cb684-110">Data type:</span></span>  <br/> |<span data-ttu-id="cb684-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="cb684-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="cb684-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cb684-112">Area:</span></span>  <br/> |<span data-ttu-id="cb684-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="cb684-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb684-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb684-114">Remarks</span></span>

<span data-ttu-id="cb684-115">Esta propiedad se usa para solicitar la correlación de los informes entrantes con el mensaje enviado original.</span><span class="sxs-lookup"><span data-stu-id="cb684-115">This property is used to request the correlation of incoming reports with the original sent message.</span></span> <span data-ttu-id="cb684-116">Cuando un proveedor de transporte encuentra un mensaje enviado con **PR_CORRELATE** establecido en true, establece la propiedad **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) en el identificador del sistema de transferencia de mensajes (mts) para ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="cb684-116">When a transport provider encounters a submitted message with **PR_CORRELATE** set to TRUE, it sets the **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) property to the message transfer system (MTS) identifier for that message.</span></span>
  
 <span data-ttu-id="cb684-117">**PR_CORRELATE** debe usarse con sistemas de mensajería que admitan la correlación por identificador de MTS, como X. 400.</span><span class="sxs-lookup"><span data-stu-id="cb684-117">**PR_CORRELATE** should be used with messaging systems that support correlation by MTS identifier, such as X.400.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cb684-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb684-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cb684-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cb684-119">Header files</span></span>

<span data-ttu-id="cb684-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cb684-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="cb684-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cb684-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="cb684-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="cb684-122">Mapitags.h</span></span>
  
> <span data-ttu-id="cb684-123">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="cb684-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb684-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb684-124">See also</span></span>



[<span data-ttu-id="cb684-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cb684-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cb684-126">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="cb684-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cb684-127">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cb684-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cb684-128">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="cb684-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

