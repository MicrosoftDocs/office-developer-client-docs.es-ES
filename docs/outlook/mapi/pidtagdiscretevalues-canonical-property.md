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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360826"
---
# <a name="pidtagdiscretevalues-canonical-property"></a><span data-ttu-id="2d286-103">Propiedad canónica PidTagDiscreteValues</span><span class="sxs-lookup"><span data-stu-id="2d286-103">PidTagDiscreteValues Canonical Property</span></span>

  
  
<span data-ttu-id="2d286-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d286-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d286-105">Contiene TRUE si un informe de no entrega solo se aplica a los miembros discretos de una lista de distribución en lugar de a toda la lista.</span><span class="sxs-lookup"><span data-stu-id="2d286-105">Contains TRUE if a nondelivery report applies only to discrete members of a distribution list rather than the entire list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2d286-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2d286-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2d286-107">PR_DISCRETE_VALUES</span><span class="sxs-lookup"><span data-stu-id="2d286-107">PR_DISCRETE_VALUES</span></span>  <br/> |
|<span data-ttu-id="2d286-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2d286-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2d286-109">0x0E0E</span><span class="sxs-lookup"><span data-stu-id="2d286-109">0x0E0E</span></span>  <br/> |
|<span data-ttu-id="2d286-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2d286-110">Data type:</span></span>  <br/> |<span data-ttu-id="2d286-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2d286-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2d286-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2d286-112">Area:</span></span>  <br/> |<span data-ttu-id="2d286-113">MAPI no transmitible</span><span class="sxs-lookup"><span data-stu-id="2d286-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d286-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2d286-114">Remarks</span></span>

<span data-ttu-id="2d286-115">Esta propiedad se usa dentro de un informe de no entrega cuando no se pudo entregar el mensaje a uno o varios miembros de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="2d286-115">This property is used within a nondelivery report when the message could not be delivered to one or more members of a distribution list.</span></span> <span data-ttu-id="2d286-116">Su objetivo es limitar los intentos de retransmisión a los miembros individuales y no a la lista de distribución en general.</span><span class="sxs-lookup"><span data-stu-id="2d286-116">Its purpose is to limit retransmission attempts to only those individual members and not the distribution list as a whole.</span></span> 
  
<span data-ttu-id="2d286-117">La tabla de destinatarios de un informe de no entrega contiene entradas para todos los destinatarios a los que no se pudo entregar el mensaje y también para las listas de distribución, si las hay, a las que pertenecen.</span><span class="sxs-lookup"><span data-stu-id="2d286-117">The recipient table of a nondelivery report contains entries for all recipients to whom the message could not be delivered, and also for the distribution lists, if any, to which they belong.</span></span> <span data-ttu-id="2d286-118">El proveedor de transporte debe establecer esta propiedad en TRUE para cada entrada de la lista de distribución y debe copiar los **PR_DISPLAY_NAME** (PidTagDisplayName \*\*\*\* ),[](pidtagdisplayname-canonical-property.md)([PidTagEntryId](pidtagentryid-canonical-property.md)) y **PR_SEARCH_KEY** ([ PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de la lista de distribución a **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) y **PR_ORIGINAL_SEARCH_KEY** ([ PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) las propiedades de cada miembro de esa lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="2d286-118">The transport provider should set this property to TRUE for each distribution list entry, and it should copy the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) from the distribution list to **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)), and **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) properties for each member of that distribution list.</span></span> 
  
 <span data-ttu-id="2d286-119">**PR_DISCRETE_VALUES** no se debe establecer para ninguna entrada de destinatario de informe de no entrega que no sea una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="2d286-119">**PR_DISCRETE_VALUES** should not be set for any nondelivery report recipient entry other than a distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2d286-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d286-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2d286-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2d286-121">Header files</span></span>

<span data-ttu-id="2d286-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2d286-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="2d286-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2d286-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="2d286-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2d286-124">Mapitags.h</span></span>
  
> <span data-ttu-id="2d286-125">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="2d286-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2d286-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d286-126">See also</span></span>



[<span data-ttu-id="2d286-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2d286-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2d286-128">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="2d286-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2d286-129">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2d286-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2d286-130">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2d286-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

