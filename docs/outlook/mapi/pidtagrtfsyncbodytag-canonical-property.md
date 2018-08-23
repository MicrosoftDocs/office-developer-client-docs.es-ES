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
ms.openlocfilehash: c141ce5b4a8d44cc42a070d73e8e89f35e776fe9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576861"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a><span data-ttu-id="2ca5e-103">Propiedad canónica PidTagRtfSyncBodyTag</span><span class="sxs-lookup"><span data-stu-id="2ca5e-103">PidTagRtfSyncBodyTag Canonical Property</span></span>

  
  
<span data-ttu-id="2ca5e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ca5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ca5e-105">Contiene caracteres significativos que aparecen al principio del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="2ca5e-105">Contains significant characters that appear at the beginning of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ca5e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2ca5e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ca5e-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span><span class="sxs-lookup"><span data-stu-id="2ca5e-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span></span>  <br/> |
|<span data-ttu-id="2ca5e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2ca5e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ca5e-109">0 x 1008</span><span class="sxs-lookup"><span data-stu-id="2ca5e-109">0x1008</span></span>  <br/> |
|<span data-ttu-id="2ca5e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2ca5e-110">Data type:</span></span>  <br/> |<span data-ttu-id="2ca5e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2ca5e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2ca5e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2ca5e-112">Area:</span></span>  <br/> |<span data-ttu-id="2ca5e-113">Mensaje MAPI</span><span class="sxs-lookup"><span data-stu-id="2ca5e-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ca5e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2ca5e-114">Remarks</span></span>

<span data-ttu-id="2ca5e-115">La función [RTFSync](rtfsync.md) utiliza la etiqueta de texto para indicar el principio del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="2ca5e-115">The [RTFSync](rtfsync.md) function uses the text tag to indicate the beginning of the message text.</span></span> <span data-ttu-id="2ca5e-116">Cuando se modifica el texto, la etiqueta se usa para buscar el principio del texto anterior.</span><span class="sxs-lookup"><span data-stu-id="2ca5e-116">When the text is modified, the tag is used to find the beginning of the previous text.</span></span> 
  
<span data-ttu-id="2ca5e-117">Estas propiedades son propiedades auxiliares de formato de texto enriquecido.</span><span class="sxs-lookup"><span data-stu-id="2ca5e-117">These properties are Rich Text Format auxiliary properties.</span></span> <span data-ttu-id="2ca5e-118">Se utilizan por la función **RTFSync** y no están diseñados para usarse directamente por las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="2ca5e-118">They are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2ca5e-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ca5e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ca5e-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="2ca5e-120">Protocol specifications</span></span>

<span data-ttu-id="2ca5e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ca5e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ca5e-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="2ca5e-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2ca5e-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ca5e-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ca5e-124">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="2ca5e-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2ca5e-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2ca5e-125">Header files</span></span>

<span data-ttu-id="2ca5e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ca5e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ca5e-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2ca5e-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="2ca5e-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2ca5e-128">Mapitags.h</span></span>
  
> <span data-ttu-id="2ca5e-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2ca5e-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ca5e-130">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="2ca5e-130">See also</span></span>



[<span data-ttu-id="2ca5e-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2ca5e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ca5e-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="2ca5e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ca5e-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2ca5e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ca5e-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="2ca5e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

