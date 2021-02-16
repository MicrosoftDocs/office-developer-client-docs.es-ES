---
title: Propiedad canónica PidTagSwappedToDoStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoStore
api_type:
- COM
ms.assetid: 1edae9ac-fc9a-4bfe-b053-99de848c5144
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 41aa97a52176cf68775d6fd507d3d042888092cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358908"
---
# <a name="pidtagswappedtodostore-canonical-property"></a><span data-ttu-id="7de93-103">Propiedad canónica PidTagSwappedToDoStore</span><span class="sxs-lookup"><span data-stu-id="7de93-103">PidTagSwappedToDoStore Canonical Property</span></span>

  
  
<span data-ttu-id="7de93-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7de93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7de93-105">Determina la necesidad de procesamiento posterior a la transmisión de un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="7de93-105">Determines the need for post-transmit processing of an email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7de93-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7de93-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7de93-107">PR_SWAPPED_TODO_STORE</span><span class="sxs-lookup"><span data-stu-id="7de93-107">PR_SWAPPED_TODO_STORE</span></span>  <br/> |
|<span data-ttu-id="7de93-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7de93-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7de93-109">0x0E2C</span><span class="sxs-lookup"><span data-stu-id="7de93-109">0x0E2C</span></span>  <br/> |
|<span data-ttu-id="7de93-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7de93-110">Data type:</span></span>  <br/> |<span data-ttu-id="7de93-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7de93-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7de93-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7de93-112">Area:</span></span>  <br/> |<span data-ttu-id="7de93-113">MAPI no transmitible</span><span class="sxs-lookup"><span data-stu-id="7de93-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7de93-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7de93-114">Remarks</span></span>

<span data-ttu-id="7de93-115">Si esta propiedad se establece en un borrador de mensaje, su valor debe establecerse en el valor de la propiedad **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="7de93-115">If this property is set on a draft message, then its value must be set to the value of **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property of the message.</span></span>
  
<span data-ttu-id="7de93-116">Para obtener más información, [vea la sección [MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) "Procesamiento posterior a la transmisión de un mensaje marcado".</span><span class="sxs-lookup"><span data-stu-id="7de93-116">For more information, see [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) section "Post-Transmit Processing of a Flagged Message."</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7de93-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7de93-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7de93-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="7de93-118">Protocol specifications</span></span>

<span data-ttu-id="7de93-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7de93-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7de93-120">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="7de93-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7de93-121">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7de93-121">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7de93-122">Especifica las propiedades y operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="7de93-122">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="7de93-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7de93-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7de93-124">Especifica las propiedades y el modelo de interacción para el correo electrónico y otros avisos de objetos.</span><span class="sxs-lookup"><span data-stu-id="7de93-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7de93-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7de93-125">Header files</span></span>

<span data-ttu-id="7de93-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7de93-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7de93-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7de93-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="7de93-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7de93-128">Mapitags.h</span></span>
  
> <span data-ttu-id="7de93-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7de93-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7de93-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7de93-130">See also</span></span>



[<span data-ttu-id="7de93-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7de93-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7de93-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="7de93-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7de93-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7de93-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7de93-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="7de93-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

