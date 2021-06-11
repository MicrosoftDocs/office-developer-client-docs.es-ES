---
title: Propiedad canónica PidTagRtfSyncPrefixCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncPrefixCount
api_type:
- COM
ms.assetid: c2b15ac5-9e89-4ee2-812d-102d0b2ac56e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 61683534504b7451f126591af149d11306cff1bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357865"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a><span data-ttu-id="9b783-103">Propiedad canónica PidTagRtfSyncPrefixCount</span><span class="sxs-lookup"><span data-stu-id="9b783-103">PidTagRtfSyncPrefixCount Canonical Property</span></span>

  
  
<span data-ttu-id="9b783-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b783-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b783-105">Contiene un recuento de los caracteres ignorables que aparecen delante de los caracteres significativos del mensaje.</span><span class="sxs-lookup"><span data-stu-id="9b783-105">Contains a count of the ignorable characters that appear before the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9b783-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9b783-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9b783-107">PR_RTF_SYNC_PREFIX_COUNT</span><span class="sxs-lookup"><span data-stu-id="9b783-107">PR_RTF_SYNC_PREFIX_COUNT</span></span>  <br/> |
|<span data-ttu-id="9b783-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9b783-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9b783-109">0x1010</span><span class="sxs-lookup"><span data-stu-id="9b783-109">0x1010</span></span>  <br/> |
|<span data-ttu-id="9b783-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9b783-110">Data type:</span></span>  <br/> |<span data-ttu-id="9b783-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9b783-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9b783-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9b783-112">Area:</span></span>  <br/> |<span data-ttu-id="9b783-113">Mensaje MAPI</span><span class="sxs-lookup"><span data-stu-id="9b783-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b783-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9b783-114">Remarks</span></span>

<span data-ttu-id="9b783-115">El recuento de caracteres de prefijo no incluye espacios en blanco.</span><span class="sxs-lookup"><span data-stu-id="9b783-115">The count of prefix characters does not include white space.</span></span>
  
<span data-ttu-id="9b783-116">Esta propiedad es una propiedad auxiliar de formato de texto enriquecido (RTF).</span><span class="sxs-lookup"><span data-stu-id="9b783-116">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="9b783-117">Las propiedades auxiliares RTF las usa la [función RTFSync](rtfsync.md) y no están diseñadas para ser usadas directamente por las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="9b783-117">RTF auxiliary properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9b783-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b783-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9b783-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="9b783-119">Protocol specifications</span></span>

<span data-ttu-id="9b783-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b783-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b783-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="9b783-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9b783-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b783-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b783-123">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficiente.</span><span class="sxs-lookup"><span data-stu-id="9b783-123">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9b783-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9b783-124">Header files</span></span>

<span data-ttu-id="9b783-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9b783-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9b783-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9b783-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="9b783-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9b783-127">Mapitags.h</span></span>
  
> <span data-ttu-id="9b783-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="9b783-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b783-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b783-129">See also</span></span>



[<span data-ttu-id="9b783-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9b783-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9b783-131">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="9b783-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9b783-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9b783-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9b783-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="9b783-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

