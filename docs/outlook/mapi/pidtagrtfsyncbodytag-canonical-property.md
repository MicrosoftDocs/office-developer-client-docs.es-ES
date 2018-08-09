---
title: Propiedad canónica PidTagRtfSyncBodyTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyTag
api_type:
- COM
ms.assetid: 2dab5018-4214-4162-93bc-e5565f3ac24c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bad754d21652d3f5278a6dad3ec06f4a0b533036
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820155"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a><span data-ttu-id="d7574-103">Propiedad canónica PidTagRtfSyncBodyTag</span><span class="sxs-lookup"><span data-stu-id="d7574-103">PidTagRtfSyncBodyTag Canonical Property</span></span>

  
  
<span data-ttu-id="d7574-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7574-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7574-105">Contiene caracteres significativos que aparecen al principio del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d7574-105">Contains significant characters that appear at the beginning of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7574-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d7574-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7574-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span><span class="sxs-lookup"><span data-stu-id="d7574-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span></span>  <br/> |
|<span data-ttu-id="d7574-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d7574-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d7574-109">0 x 1008</span><span class="sxs-lookup"><span data-stu-id="d7574-109">0x1008</span></span>  <br/> |
|<span data-ttu-id="d7574-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d7574-110">Data type:</span></span>  <br/> |<span data-ttu-id="d7574-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d7574-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d7574-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d7574-112">Area:</span></span>  <br/> |<span data-ttu-id="d7574-113">Mensaje MAPI</span><span class="sxs-lookup"><span data-stu-id="d7574-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7574-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d7574-114">Remarks</span></span>

<span data-ttu-id="d7574-115">La función [RTFSync](rtfsync.md) utiliza la etiqueta de texto para indicar el principio del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d7574-115">The [RTFSync](rtfsync.md) function uses the text tag to indicate the beginning of the message text.</span></span> <span data-ttu-id="d7574-116">Cuando se modifica el texto, la etiqueta se usa para buscar el principio del texto anterior.</span><span class="sxs-lookup"><span data-stu-id="d7574-116">When the text is modified, the tag is used to find the beginning of the previous text.</span></span> 
  
<span data-ttu-id="d7574-117">Estas propiedades son propiedades auxiliares de formato de texto enriquecido.</span><span class="sxs-lookup"><span data-stu-id="d7574-117">These properties are Rich Text Format auxiliary properties.</span></span> <span data-ttu-id="d7574-118">Se utilizan por la función **RTFSync** y no están diseñados para usarse directamente por las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="d7574-118">They are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d7574-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7574-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d7574-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d7574-120">Protocol specifications</span></span>

<span data-ttu-id="d7574-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7574-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7574-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d7574-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d7574-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7574-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7574-124">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="d7574-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d7574-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d7574-125">Header files</span></span>

<span data-ttu-id="d7574-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7574-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7574-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d7574-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="d7574-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d7574-128">Mapitags.h</span></span>
  
> <span data-ttu-id="d7574-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d7574-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7574-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7574-130">See also</span></span>



[<span data-ttu-id="d7574-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d7574-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7574-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d7574-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7574-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d7574-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7574-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d7574-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

