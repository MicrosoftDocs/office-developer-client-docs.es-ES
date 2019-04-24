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
ms.openlocfilehash: 24ef1d4e3e936426aea8216119e8ada9f6122e95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331181"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a><span data-ttu-id="13f43-103">Propiedad canónica PidTagRtfSyncBodyTag</span><span class="sxs-lookup"><span data-stu-id="13f43-103">PidTagRtfSyncBodyTag Canonical Property</span></span>

  
  
<span data-ttu-id="13f43-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13f43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13f43-105">Contiene los caracteres significativos que aparecen al principio del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="13f43-105">Contains significant characters that appear at the beginning of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13f43-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="13f43-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13f43-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span><span class="sxs-lookup"><span data-stu-id="13f43-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span></span>  <br/> |
|<span data-ttu-id="13f43-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="13f43-108">Identifier:</span></span>  <br/> |<span data-ttu-id="13f43-109">0x1008</span><span class="sxs-lookup"><span data-stu-id="13f43-109">0x1008</span></span>  <br/> |
|<span data-ttu-id="13f43-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="13f43-110">Data type:</span></span>  <br/> |<span data-ttu-id="13f43-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="13f43-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="13f43-112">Área:</span><span class="sxs-lookup"><span data-stu-id="13f43-112">Area:</span></span>  <br/> |<span data-ttu-id="13f43-113">Mensaje MAPI</span><span class="sxs-lookup"><span data-stu-id="13f43-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13f43-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13f43-114">Remarks</span></span>

<span data-ttu-id="13f43-115">La función [RTFSync](rtfsync.md) usa la etiqueta Text para indicar el principio del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="13f43-115">The [RTFSync](rtfsync.md) function uses the text tag to indicate the beginning of the message text.</span></span> <span data-ttu-id="13f43-116">Cuando se modifica el texto, la etiqueta se usa para buscar el principio del texto anterior.</span><span class="sxs-lookup"><span data-stu-id="13f43-116">When the text is modified, the tag is used to find the beginning of the previous text.</span></span> 
  
<span data-ttu-id="13f43-117">Estas propiedades son propiedades auxiliares de formato de texto enriquecido (RTF).</span><span class="sxs-lookup"><span data-stu-id="13f43-117">These properties are Rich Text Format auxiliary properties.</span></span> <span data-ttu-id="13f43-118">La función **RTFSync** la usan y no está pensada para que las usen directamente las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="13f43-118">They are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="13f43-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="13f43-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13f43-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="13f43-120">Protocol specifications</span></span>

<span data-ttu-id="13f43-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13f43-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13f43-122">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="13f43-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13f43-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13f43-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13f43-124">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="13f43-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13f43-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="13f43-125">Header files</span></span>

<span data-ttu-id="13f43-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="13f43-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="13f43-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="13f43-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="13f43-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="13f43-128">Mapitags.h</span></span>
  
> <span data-ttu-id="13f43-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="13f43-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13f43-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="13f43-130">See also</span></span>



[<span data-ttu-id="13f43-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="13f43-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13f43-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="13f43-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13f43-133">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="13f43-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13f43-134">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="13f43-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

