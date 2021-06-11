---
title: Propiedad canónica PidTagSubjectPrefix
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubjectPrefix
api_type:
- COM
ms.assetid: 07fcb881-d873-45bf-b048-30f41d0d8d85
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8257c3c3583072d16e96e6ea9bba4632fc78f9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339231"
---
# <a name="pidtagsubjectprefix-canonical-property"></a><span data-ttu-id="a71a0-103">Propiedad canónica PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="a71a0-103">PidTagSubjectPrefix Canonical Property</span></span>

  
  
<span data-ttu-id="a71a0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a71a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a71a0-105">Contiene un prefijo de asunto que normalmente indica alguna acción en un mensaje, como "FW: " para reenviar.</span><span class="sxs-lookup"><span data-stu-id="a71a0-105">Contains a subject prefix that typically indicates some action on a message, such as "FW: " for forwarding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a71a0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a71a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a71a0-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span><span class="sxs-lookup"><span data-stu-id="a71a0-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span></span>  <br/> |
|<span data-ttu-id="a71a0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a71a0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a71a0-109">0x003D</span><span class="sxs-lookup"><span data-stu-id="a71a0-109">0x003D</span></span>  <br/> |
|<span data-ttu-id="a71a0-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a71a0-110">Data type:</span></span>  <br/> |<span data-ttu-id="a71a0-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a71a0-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a71a0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a71a0-112">Area:</span></span>  <br/> |<span data-ttu-id="a71a0-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="a71a0-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a71a0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a71a0-114">Remarks</span></span>

<span data-ttu-id="a71a0-115">Estas propiedades se recomiendan en todos los objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a71a0-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="a71a0-116">El prefijo de sujeto consta de uno o más caracteres alfanuméricos, seguidos de dos puntos y un espacio (que forman parte del prefijo).</span><span class="sxs-lookup"><span data-stu-id="a71a0-116">The subject prefix consists of one or more alphanumeric characters, followed by a colon and a space (which are part of the prefix).</span></span> <span data-ttu-id="a71a0-117">No debe contener ningún carácter nonalphanumeric delante de los dos puntos.</span><span class="sxs-lookup"><span data-stu-id="a71a0-117">It must not contain any nonalphanumeric characters before the colon.</span></span> <span data-ttu-id="a71a0-118">La ausencia de un prefijo puede representarse mediante una cadena vacía o por esta propiedad que no se está configurando.</span><span class="sxs-lookup"><span data-stu-id="a71a0-118">Absence of a prefix can be represented by an empty string or by this property not being set.</span></span> 
  
<span data-ttu-id="a71a0-119">Si estas propiedades se establecen explícitamente, la cadena puede ser de cualquier longitud y usar cualquier carácter alfanumérico, pero debe coincidir con una subcadena al principio de la propiedad **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a71a0-119">If these properties are set explicitly, the string can be of any length and use any alphanumeric characters, but it must match a substring at the beginning of the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="a71a0-120">Si el remitente no establece estas propiedades y debe calcularse, su contenido está más restringido.</span><span class="sxs-lookup"><span data-stu-id="a71a0-120">If these properties are not set by the sender and must be computed, their contents are more restricted.</span></span> <span data-ttu-id="a71a0-121">La regla para calcular el prefijo es **que PR_SUBJECT** debe comenzar con una, dos o tres letras (solo alfabéticas) seguidas de dos puntos y un espacio.</span><span class="sxs-lookup"><span data-stu-id="a71a0-121">The rule for computing the prefix is that **PR_SUBJECT** must begin with one, two, or three letters (alphabetic only) followed by a colon and a space.</span></span> <span data-ttu-id="a71a0-122">Si dicha subcadena se encuentra al principio de **PR_SUBJECT**, se convierte en la cadena de estas propiedades (y también permanece al principio de **PR_SUBJECT**).</span><span class="sxs-lookup"><span data-stu-id="a71a0-122">If such a substring is found at the beginning of **PR_SUBJECT**, it then becomes the string for these properties (and also stays at the beginning of **PR_SUBJECT**).</span></span> <span data-ttu-id="a71a0-123">De lo contrario, estas propiedades permanecen sin conjunto.</span><span class="sxs-lookup"><span data-stu-id="a71a0-123">Otherwise, these properties remain unset.</span></span> 
  
<span data-ttu-id="a71a0-124">Estas propiedades **y PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) deben calcularse como parte de la [implementación IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="a71a0-124">These properties and **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="a71a0-125">Un cliente no debe solicitar [a IMAPIProp::GetProps](imapiprop-getprops.md) sus valores hasta que se hayan confirmado mediante una llamada **IMAPIProp::SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="a71a0-125">A client should not prompt [IMAPIProp::GetProps](imapiprop-getprops.md) for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="a71a0-126">Las propiedades del asunto suelen ser pequeñas cadenas de menos de 256 caracteres y un proveedor de almacén de mensajes no está obligado a admitir la interfaz **OLE IStream** en ellas.</span><span class="sxs-lookup"><span data-stu-id="a71a0-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the OLE **IStream** interface on them.</span></span> <span data-ttu-id="a71a0-127">Un cliente siempre debe intentar el acceso a través de la interfaz **IMAPIProp** primero y recurrir a **IStream** solo **si MAPI_E_NOT_ENOUGH_MEMORY** se devuelve.</span><span class="sxs-lookup"><span data-stu-id="a71a0-127">A client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a71a0-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a71a0-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a71a0-129">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="a71a0-129">Protocol specifications</span></span>

<span data-ttu-id="a71a0-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a71a0-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a71a0-131">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="a71a0-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a71a0-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a71a0-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a71a0-133">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a71a0-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="a71a0-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a71a0-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a71a0-135">Especifica las propiedades y las operaciones permitidas en objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a71a0-135">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a71a0-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a71a0-136">Header files</span></span>

<span data-ttu-id="a71a0-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a71a0-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="a71a0-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a71a0-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="a71a0-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a71a0-139">Mapitags.h</span></span>
  
> <span data-ttu-id="a71a0-140">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a71a0-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a71a0-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="a71a0-141">See also</span></span>



[<span data-ttu-id="a71a0-142">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a71a0-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a71a0-143">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a71a0-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a71a0-144">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a71a0-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a71a0-145">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="a71a0-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

