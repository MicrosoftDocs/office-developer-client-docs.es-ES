---
title: Propiedad canónica PidTagRtfSyncTrailingCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncTrailingCount
api_type:
- COM
ms.assetid: 3f0e5b24-767e-46f5-bb3d-e9cb82cb935b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3174ebbcf70104c82305e2a20df1e183d30265d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820143"
---
# <a name="pidtagrtfsynctrailingcount-canonical-property"></a><span data-ttu-id="be7b5-103">Propiedad canónica PidTagRtfSyncTrailingCount</span><span class="sxs-lookup"><span data-stu-id="be7b5-103">PidTagRtfSyncTrailingCount Canonical Property</span></span>

  
  
<span data-ttu-id="be7b5-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="be7b5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="be7b5-105">Contiene un recuento de los caracteres puede pasar por alto que aparecen después de los caracteres del mensaje significativos.</span><span class="sxs-lookup"><span data-stu-id="be7b5-105">Contains a count of the ignorable characters that appear after the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be7b5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="be7b5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="be7b5-107">PR_RTF_SYNC_TRAILING_COUNT</span><span class="sxs-lookup"><span data-stu-id="be7b5-107">PR_RTF_SYNC_TRAILING_COUNT</span></span>  <br/> |
|<span data-ttu-id="be7b5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="be7b5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="be7b5-109">0x1011</span><span class="sxs-lookup"><span data-stu-id="be7b5-109">0x1011</span></span>  <br/> |
|<span data-ttu-id="be7b5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="be7b5-110">Data type:</span></span>  <br/> |<span data-ttu-id="be7b5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="be7b5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="be7b5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="be7b5-112">Area:</span></span>  <br/> |<span data-ttu-id="be7b5-113">Mensaje MAPI</span><span class="sxs-lookup"><span data-stu-id="be7b5-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be7b5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be7b5-114">Remarks</span></span>

<span data-ttu-id="be7b5-115">Esta propiedad es una propiedad auxiliar de formato de texto enriquecido (RTF).</span><span class="sxs-lookup"><span data-stu-id="be7b5-115">This property is a Rich Text Format (RFT) auxiliary property.</span></span> <span data-ttu-id="be7b5-116">Estas propiedades se usan por la función [RTFSync](rtfsync.md) y no están diseñadas para usarse directamente por las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="be7b5-116">These properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="be7b5-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="be7b5-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="be7b5-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="be7b5-118">Protocol specifications</span></span>

<span data-ttu-id="be7b5-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be7b5-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be7b5-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="be7b5-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="be7b5-121">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be7b5-121">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be7b5-122">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="be7b5-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="be7b5-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="be7b5-123">Header files</span></span>

<span data-ttu-id="be7b5-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be7b5-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="be7b5-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="be7b5-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="be7b5-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="be7b5-126">Mapitags.h</span></span>
  
> <span data-ttu-id="be7b5-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="be7b5-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be7b5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="be7b5-128">See also</span></span>



[<span data-ttu-id="be7b5-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="be7b5-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be7b5-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="be7b5-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be7b5-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="be7b5-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be7b5-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="be7b5-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

