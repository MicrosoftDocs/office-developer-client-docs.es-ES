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
ms.openlocfilehash: f1aa54c3364185d322137ef41f6aface31c5c556
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587421"
---
# <a name="pidtagdiscretevalues-canonical-property"></a><span data-ttu-id="9f9e1-103">Propiedad canónica PidTagDiscreteValues</span><span class="sxs-lookup"><span data-stu-id="9f9e1-103">PidTagDiscreteValues Canonical Property</span></span>

  
  
<span data-ttu-id="9f9e1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f9e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f9e1-105">Contiene TRUE si un informe de no entrega aplica a sólo a discretos miembros de una lista de distribución en lugar de toda la lista.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-105">Contains TRUE if a nondelivery report applies only to discrete members of a distribution list rather than the entire list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f9e1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9f9e1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9f9e1-107">PR_DISCRETE_VALUES</span><span class="sxs-lookup"><span data-stu-id="9f9e1-107">PR_DISCRETE_VALUES</span></span>  <br/> |
|<span data-ttu-id="9f9e1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9f9e1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9f9e1-109">0x0E0E</span><span class="sxs-lookup"><span data-stu-id="9f9e1-109">0x0E0E</span></span>  <br/> |
|<span data-ttu-id="9f9e1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9f9e1-110">Data type:</span></span>  <br/> |<span data-ttu-id="9f9e1-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9f9e1-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9f9e1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9f9e1-112">Area:</span></span>  <br/> |<span data-ttu-id="9f9e1-113">MAPI no transmisible</span><span class="sxs-lookup"><span data-stu-id="9f9e1-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f9e1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f9e1-114">Remarks</span></span>

<span data-ttu-id="9f9e1-115">Esta propiedad se usa dentro de un informe de no entrega cuando no se pudo entregar el mensaje a uno o varios miembros de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-115">This property is used within a nondelivery report when the message could not be delivered to one or more members of a distribution list.</span></span> <span data-ttu-id="9f9e1-116">Su objetivo es limitar la retransmisión intenta sólo los miembros individuales y no la lista de distribución como un todo.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-116">Its purpose is to limit retransmission attempts to only those individual members and not the distribution list as a whole.</span></span> 
  
<span data-ttu-id="9f9e1-117">La tabla de destinatarios de un informe de no entrega contiene entradas para todos los destinatarios a quienes el mensaje no se pudo entregar y también para las listas de distribución, si lo hay, al que pertenecen.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-117">The recipient table of a nondelivery report contains entries for all recipients to whom the message could not be delivered, and also for the distribution lists, if any, to which they belong.</span></span> <span data-ttu-id="9f9e1-118">El proveedor de transporte debe establecer esta propiedad en TRUE para cada entrada de la lista de distribución, y deben copiar el **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) y el **PR_SEARCH_KEY** ([ PidTagSearchKey](pidtagsearchkey-canonical-property.md)) en la lista de distribución para **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) y **PR_ORIGINAL_SEARCH_KEY** ([ PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) propiedades para cada miembro de esa lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-118">The transport provider should set this property to TRUE for each distribution list entry, and it should copy the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) from the distribution list to **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)), and **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) properties for each member of that distribution list.</span></span> 
  
 <span data-ttu-id="9f9e1-119">**PR_DISCRETE_VALUES** no se debe establecer para cualquier entrada destinatario del informe de no entrega que no sea una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-119">**PR_DISCRETE_VALUES** should not be set for any nondelivery report recipient entry other than a distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9f9e1-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9f9e1-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9f9e1-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9f9e1-121">Header files</span></span>

<span data-ttu-id="9f9e1-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9f9e1-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="9f9e1-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="9f9e1-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9f9e1-124">Mapitags.h</span></span>
  
> <span data-ttu-id="9f9e1-125">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="9f9e1-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f9e1-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="9f9e1-126">See also</span></span>



[<span data-ttu-id="9f9e1-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9f9e1-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9f9e1-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="9f9e1-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9f9e1-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9f9e1-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9f9e1-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="9f9e1-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

