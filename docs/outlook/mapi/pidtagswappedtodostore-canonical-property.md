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
ms.openlocfilehash: cbe1915df46010c5574065826ac1814f45c8c093
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820406"
---
# <a name="pidtagswappedtodostore-canonical-property"></a><span data-ttu-id="1b51b-103">Propiedad canónica PidTagSwappedToDoStore</span><span class="sxs-lookup"><span data-stu-id="1b51b-103">PidTagSwappedToDoStore Canonical Property</span></span>

  
  
<span data-ttu-id="1b51b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b51b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b51b-105">Determina la necesidad de transmitir posteriores a la transformación de un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1b51b-105">Determines the need for post-transmit processing of an email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b51b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1b51b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b51b-107">PR_SWAPPED_TODO_STORE</span><span class="sxs-lookup"><span data-stu-id="1b51b-107">PR_SWAPPED_TODO_STORE</span></span>  <br/> |
|<span data-ttu-id="1b51b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1b51b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1b51b-109">0x0E2C</span><span class="sxs-lookup"><span data-stu-id="1b51b-109">0x0E2C</span></span>  <br/> |
|<span data-ttu-id="1b51b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1b51b-110">Data type:</span></span>  <br/> |<span data-ttu-id="1b51b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1b51b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1b51b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1b51b-112">Area:</span></span>  <br/> |<span data-ttu-id="1b51b-113">MAPI no transmisible</span><span class="sxs-lookup"><span data-stu-id="1b51b-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b51b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1b51b-114">Remarks</span></span>

<span data-ttu-id="1b51b-115">Si esta propiedad se establece en un borrador de mensaje, a continuación, su valor debe establecerse en el valor de propiedad de **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="1b51b-115">If this property is set on a draft message, then its value must be set to the value of **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property of the message.</span></span>
  
<span data-ttu-id="1b51b-116">Para obtener más información, vea [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) sección "posteriores a la transmisión de procesamiento de un mensaje marcado."</span><span class="sxs-lookup"><span data-stu-id="1b51b-116">For more information, see [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) section "Post-Transmit Processing of a Flagged Message."</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1b51b-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b51b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1b51b-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1b51b-118">Protocol specifications</span></span>

<span data-ttu-id="1b51b-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b51b-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b51b-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1b51b-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1b51b-121">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b51b-121">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b51b-122">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="1b51b-122">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="1b51b-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b51b-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b51b-124">Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.</span><span class="sxs-lookup"><span data-stu-id="1b51b-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1b51b-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1b51b-125">Header files</span></span>

<span data-ttu-id="1b51b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1b51b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b51b-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1b51b-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="1b51b-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1b51b-128">Mapitags.h</span></span>
  
> <span data-ttu-id="1b51b-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1b51b-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b51b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b51b-130">See also</span></span>



[<span data-ttu-id="1b51b-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1b51b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1b51b-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1b51b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1b51b-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1b51b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1b51b-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="1b51b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

