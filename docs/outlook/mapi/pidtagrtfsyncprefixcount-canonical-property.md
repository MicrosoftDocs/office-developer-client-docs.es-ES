---
title: Propiedad canónico PidTagRtfSyncPrefixCount
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: c9a62365b46e85cc8f5d22fd31de3b5c6bd3f76a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820141"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a><span data-ttu-id="7d0f5-103">Propiedad canónico PidTagRtfSyncPrefixCount</span><span class="sxs-lookup"><span data-stu-id="7d0f5-103">PidTagRtfSyncPrefixCount Canonical Property</span></span>

  
  
<span data-ttu-id="7d0f5-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7d0f5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7d0f5-105">Contiene un recuento de los caracteres puede pasar por alto que aparecen antes de los caracteres del mensaje significativos.</span><span class="sxs-lookup"><span data-stu-id="7d0f5-105">Contains a count of the ignorable characters that appear before the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7d0f5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7d0f5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d0f5-107">PR_RTF_SYNC_PREFIX_COUNT</span><span class="sxs-lookup"><span data-stu-id="7d0f5-107">PR_RTF_SYNC_PREFIX_COUNT</span></span>  <br/> |
|<span data-ttu-id="7d0f5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7d0f5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7d0f5-109">0x1010</span><span class="sxs-lookup"><span data-stu-id="7d0f5-109">0x1010</span></span>  <br/> |
|<span data-ttu-id="7d0f5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7d0f5-110">Data type:</span></span>  <br/> |<span data-ttu-id="7d0f5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7d0f5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7d0f5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7d0f5-112">Area:</span></span>  <br/> |<span data-ttu-id="7d0f5-113">Mensaje MAPI</span><span class="sxs-lookup"><span data-stu-id="7d0f5-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d0f5-114">Notas</span><span class="sxs-lookup"><span data-stu-id="7d0f5-114">Remarks</span></span>

<span data-ttu-id="7d0f5-115">El número de caracteres de prefijo no incluya espacios en blanco.</span><span class="sxs-lookup"><span data-stu-id="7d0f5-115">The count of prefix characters does not include white space.</span></span>
  
<span data-ttu-id="7d0f5-116">Esta propiedad es una propiedad auxiliar de formato de texto enriquecido (RTF).</span><span class="sxs-lookup"><span data-stu-id="7d0f5-116">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="7d0f5-117">Propiedades auxiliares RTF se usan por la función [RTFSync](rtfsync.md) y no están diseñadas para usarse directamente por las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="7d0f5-117">RTF auxiliary properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7d0f5-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d0f5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7d0f5-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="7d0f5-119">Protocol specifications</span></span>

<span data-ttu-id="7d0f5-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d0f5-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d0f5-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7d0f5-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7d0f5-122">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d0f5-122">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d0f5-123">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="7d0f5-123">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7d0f5-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7d0f5-124">Header files</span></span>

<span data-ttu-id="7d0f5-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d0f5-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d0f5-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7d0f5-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="7d0f5-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7d0f5-127">Mapitags.h</span></span>
  
> <span data-ttu-id="7d0f5-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7d0f5-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d0f5-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="7d0f5-129">See also</span></span>



[<span data-ttu-id="7d0f5-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7d0f5-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d0f5-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="7d0f5-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d0f5-132">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="7d0f5-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d0f5-133">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7d0f5-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

