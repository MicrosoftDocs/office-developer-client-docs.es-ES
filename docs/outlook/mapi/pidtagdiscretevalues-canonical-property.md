---
title: Propiedad canónica PidTagDiscreteValues
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscreteValues
api_type:
- HeaderDef
ms.assetid: 958f3cf7-953a-43f4-9102-ad35edf5e813
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6d6974302e3413db3590abbbd3e6567976c6ac72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404844"
---
# <a name="pidtagdiscretevalues-canonical-property"></a><span data-ttu-id="fc976-103">Propiedad canónica PidTagDiscreteValues</span><span class="sxs-lookup"><span data-stu-id="fc976-103">PidTagDiscreteValues Canonical Property</span></span>

  
  
<span data-ttu-id="fc976-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc976-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc976-105">Contiene TRUE si un informe de no entrega solo se aplica a miembros discretos de una lista de distribución en lugar de a toda la lista.</span><span class="sxs-lookup"><span data-stu-id="fc976-105">Contains TRUE if a nondelivery report applies only to discrete members of a distribution list rather than the entire list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc976-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fc976-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc976-107">PR_DISCRETE_VALUES</span><span class="sxs-lookup"><span data-stu-id="fc976-107">PR_DISCRETE_VALUES</span></span>  <br/> |
|<span data-ttu-id="fc976-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fc976-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fc976-109">0x0E0E</span><span class="sxs-lookup"><span data-stu-id="fc976-109">0x0E0E</span></span>  <br/> |
|<span data-ttu-id="fc976-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fc976-110">Data type:</span></span>  <br/> |<span data-ttu-id="fc976-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="fc976-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="fc976-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fc976-112">Area:</span></span>  <br/> |<span data-ttu-id="fc976-113">MAPI no transmitible</span><span class="sxs-lookup"><span data-stu-id="fc976-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc976-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fc976-114">Remarks</span></span>

<span data-ttu-id="fc976-115">Esta propiedad se usa en un informe de no entrega cuando el mensaje no se pudo entregar a uno o varios miembros de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="fc976-115">This property is used within a nondelivery report when the message could not be delivered to one or more members of a distribution list.</span></span> <span data-ttu-id="fc976-116">Su objetivo es limitar los intentos de retransmisión solo a los miembros individuales y no a la lista de distribución en su conjunto.</span><span class="sxs-lookup"><span data-stu-id="fc976-116">Its purpose is to limit retransmission attempts to only those individual members and not the distribution list as a whole.</span></span> 
  
<span data-ttu-id="fc976-117">La tabla de destinatarios de un informe de no entrega contiene entradas para todos los destinatarios a los que no se pudo entregar el mensaje y también para las listas de distribución, si las hay, a las que pertenecen.</span><span class="sxs-lookup"><span data-stu-id="fc976-117">The recipient table of a nondelivery report contains entries for all recipients to whom the message could not be delivered, and also for the distribution lists, if any, to which they belong.</span></span> <span data-ttu-id="fc976-118">El proveedor de transporte debe establecer esta propiedad en TRUE para cada entrada de lista de distribución y debe copiar las propiedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) y **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de la lista de distribución a **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) y **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) para cada miembro de esa lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="fc976-118">The transport provider should set this property to TRUE for each distribution list entry, and it should copy the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) from the distribution list to **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)), and **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) properties for each member of that distribution list.</span></span> 
  
 <span data-ttu-id="fc976-119">**PR_DISCRETE_VALUES** no debe establecerse para ninguna entrada de destinatario de informe de no entrega que no sea una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="fc976-119">**PR_DISCRETE_VALUES** should not be set for any nondelivery report recipient entry other than a distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fc976-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc976-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fc976-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fc976-121">Header files</span></span>

<span data-ttu-id="fc976-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc976-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc976-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fc976-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="fc976-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fc976-124">Mapitags.h</span></span>
  
> <span data-ttu-id="fc976-125">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="fc976-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc976-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc976-126">See also</span></span>



[<span data-ttu-id="fc976-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fc976-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc976-128">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fc976-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc976-129">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fc976-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc976-130">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="fc976-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

