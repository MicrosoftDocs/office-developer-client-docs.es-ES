---
title: Propiedad canónica PidTagOriginallyIntendedRecipEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEntryId
api_type:
- COM
ms.assetid: fc288a7a-1927-484e-b860-9cc118672ed2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cf9a070e8f892cb7bd4668b3f92397070e5b2284
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342528"
---
# <a name="pidtagoriginallyintendedrecipentryid-canonical-property"></a><span data-ttu-id="eecfb-103">Propiedad canónica PidTagOriginallyIntendedRecipEntryId</span><span class="sxs-lookup"><span data-stu-id="eecfb-103">PidTagOriginallyIntendedRecipEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="eecfb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eecfb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eecfb-105">Contiene el identificador de entrada del destinatario previsto originalmente de un mensaje de reenvío automático.</span><span class="sxs-lookup"><span data-stu-id="eecfb-105">Contains the entry identifier of the originally intended recipient of an auto-forwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eecfb-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="eecfb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eecfb-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="eecfb-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="eecfb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="eecfb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eecfb-109">0x1012</span><span class="sxs-lookup"><span data-stu-id="eecfb-109">0x1012</span></span>  <br/> |
|<span data-ttu-id="eecfb-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="eecfb-110">Data type:</span></span>  <br/> |<span data-ttu-id="eecfb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="eecfb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="eecfb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="eecfb-112">Area:</span></span>  <br/> |<span data-ttu-id="eecfb-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="eecfb-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eecfb-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eecfb-114">Remarks</span></span>

<span data-ttu-id="eecfb-115">Esta propiedad es una de las propiedades de dirección del destinatario del mensaje que se diseñó originalmente.</span><span class="sxs-lookup"><span data-stu-id="eecfb-115">This property is one of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="eecfb-116">Debe establecerse mediante el agente automático que ha reenviado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="eecfb-116">It must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="eecfb-117">Esta propiedad corresponde al atributo per-recipient del informe X. 400.</span><span class="sxs-lookup"><span data-stu-id="eecfb-117">This property corresponds to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eecfb-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="eecfb-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="eecfb-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="eecfb-119">Header files</span></span>

<span data-ttu-id="eecfb-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="eecfb-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="eecfb-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="eecfb-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="eecfb-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="eecfb-122">Mapitags.h</span></span>
  
> <span data-ttu-id="eecfb-123">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="eecfb-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eecfb-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="eecfb-124">See also</span></span>



[<span data-ttu-id="eecfb-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="eecfb-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eecfb-126">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="eecfb-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eecfb-127">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="eecfb-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eecfb-128">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="eecfb-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

