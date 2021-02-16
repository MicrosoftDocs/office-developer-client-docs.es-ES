---
title: Propiedad canónica PidTagSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubject
api_type:
- COM
ms.assetid: aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0cf9e9f8c10f8d27bd174b8b6f2bf19812dc269d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339259"
---
# <a name="pidtagsubject-canonical-property"></a><span data-ttu-id="e58ed-103">Propiedad canónica PidTagSubject</span><span class="sxs-lookup"><span data-stu-id="e58ed-103">PidTagSubject Canonical Property</span></span>

  
  
<span data-ttu-id="e58ed-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e58ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e58ed-105">Contiene el asunto completo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="e58ed-105">Contains the full subject of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e58ed-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e58ed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e58ed-107">PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="e58ed-107">PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="e58ed-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e58ed-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e58ed-109">0x0037</span><span class="sxs-lookup"><span data-stu-id="e58ed-109">0x0037</span></span>  <br/> |
|<span data-ttu-id="e58ed-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e58ed-110">Data type:</span></span>  <br/> |<span data-ttu-id="e58ed-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e58ed-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e58ed-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e58ed-112">Area:</span></span>  <br/> |<span data-ttu-id="e58ed-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="e58ed-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e58ed-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e58ed-114">Remarks</span></span>

<span data-ttu-id="e58ed-115">Estas propiedades se recomiendan en todos los objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e58ed-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="e58ed-116">Estas propiedades siempre son el texto del asunto completo, es decir, la concatenación del prefijo y el asunto normalizado.</span><span class="sxs-lookup"><span data-stu-id="e58ed-116">These properties are always the full subject text, that is, the concatenation of the prefix and the normalized subject.</span></span> <span data-ttu-id="e58ed-117">Si no hay ningún prefijo, el asunto normalizado debe ser el mismo que el asunto.</span><span class="sxs-lookup"><span data-stu-id="e58ed-117">If there is no prefix, the normalized subject should be the same as the subject.</span></span> <span data-ttu-id="e58ed-118">Un almacén de mensajes o un proveedor de transporte usa estas propiedades y propiedades **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) para calcular el asunto normalizado mediante la regla descrita en **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e58ed-118">A message store or transport provider uses both these properties and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties to compute the normalized subject using the rule described under **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span></span>
  
<span data-ttu-id="e58ed-119">Las propiedades del asunto suelen ser cadenas pequeñas de menos de 256 caracteres y un proveedor de almacenamiento de mensajes no está obligado a admitir la interfaz **IStream** en ellas.</span><span class="sxs-lookup"><span data-stu-id="e58ed-119">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the **IStream** interface on them.</span></span> <span data-ttu-id="e58ed-120">El cliente siempre debe intentar obtener acceso a través de la interfaz **IMAPIProp** en primer lugar y recurrir a **IStream** solo si **MAPI_E_NOT_ENOUGH_MEMORY** se devuelve.</span><span class="sxs-lookup"><span data-stu-id="e58ed-120">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
<span data-ttu-id="e58ed-121">Para un informe, esta propiedad contiene el asunto del mensaje original precedido de una cadena que indica lo que ha ocurrido con el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e58ed-121">For a report, this property contains the original message's subject preceded by a string indicating what has happened to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e58ed-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e58ed-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e58ed-123">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="e58ed-123">Protocol specifications</span></span>

<span data-ttu-id="e58ed-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e58ed-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e58ed-125">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="e58ed-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e58ed-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e58ed-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e58ed-127">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e58ed-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e58ed-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e58ed-128">Header files</span></span>

<span data-ttu-id="e58ed-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e58ed-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="e58ed-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e58ed-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="e58ed-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e58ed-131">Mapitags.h</span></span>
  
> <span data-ttu-id="e58ed-132">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="e58ed-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e58ed-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e58ed-133">See also</span></span>



[<span data-ttu-id="e58ed-134">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e58ed-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e58ed-135">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="e58ed-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e58ed-136">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e58ed-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e58ed-137">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="e58ed-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

