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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385651"
---
# <a name="pidtagsubjectprefix-canonical-property"></a><span data-ttu-id="93a3e-103">Propiedad canónica PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="93a3e-103">PidTagSubjectPrefix Canonical Property</span></span>

  
  
<span data-ttu-id="93a3e-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93a3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93a3e-105">Contiene un prefijo de asunto que indica normalmente alguna acción en un mensaje, como "Rv:" para el reenvío.</span><span class="sxs-lookup"><span data-stu-id="93a3e-105">Contains a subject prefix that typically indicates some action on a message, such as "FW: " for forwarding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="93a3e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="93a3e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93a3e-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span><span class="sxs-lookup"><span data-stu-id="93a3e-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span></span>  <br/> |
|<span data-ttu-id="93a3e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="93a3e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="93a3e-109">0x003D</span><span class="sxs-lookup"><span data-stu-id="93a3e-109">0x003D</span></span>  <br/> |
|<span data-ttu-id="93a3e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="93a3e-110">Data type:</span></span>  <br/> |<span data-ttu-id="93a3e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="93a3e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="93a3e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="93a3e-112">Area:</span></span>  <br/> |<span data-ttu-id="93a3e-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="93a3e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93a3e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="93a3e-114">Remarks</span></span>

<span data-ttu-id="93a3e-115">Se recomienda utilizar estas propiedades en todos los objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="93a3e-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="93a3e-116">El prefijo del asunto consta de uno o más caracteres alfanuméricos, seguidos de un punto y coma y un espacio (que forman parte del prefijo).</span><span class="sxs-lookup"><span data-stu-id="93a3e-116">The subject prefix consists of one or more alphanumeric characters, followed by a colon and a space (which are part of the prefix).</span></span> <span data-ttu-id="93a3e-117">No debe contener todos los caracteres no alfanuméricos antes de los dos puntos.</span><span class="sxs-lookup"><span data-stu-id="93a3e-117">It must not contain any nonalphanumeric characters before the colon.</span></span> <span data-ttu-id="93a3e-118">Ausencia de un prefijo puede estar representada por una cadena vacía o por esta propiedad no está establecido.</span><span class="sxs-lookup"><span data-stu-id="93a3e-118">Absence of a prefix can be represented by an empty string or by this property not being set.</span></span> 
  
<span data-ttu-id="93a3e-119">Si estas propiedades se establecen de forma explícita, la cadena puede ser de cualquier longitud y usar caracteres alfanuméricos, pero debe coincidir con una subcadena al principio de la propiedad **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="93a3e-119">If these properties are set explicitly, the string can be of any length and use any alphanumeric characters, but it must match a substring at the beginning of the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="93a3e-120">Si estas propiedades no se han establecido por el remitente y deben calcularse, su contenido es más restringido.</span><span class="sxs-lookup"><span data-stu-id="93a3e-120">If these properties are not set by the sender and must be computed, their contents are more restricted.</span></span> <span data-ttu-id="93a3e-121">La regla de la informática el prefijo es que **PR_SUBJECT** debe comenzar con uno, dos o tres letras (alfabéticos sólo) seguido de un punto y coma y un espacio.</span><span class="sxs-lookup"><span data-stu-id="93a3e-121">The rule for computing the prefix is that **PR_SUBJECT** must begin with one, two, or three letters (alphabetic only) followed by a colon and a space.</span></span> <span data-ttu-id="93a3e-122">Si se encuentra dicha una subcadena al principio del **PR_SUBJECT**, a continuación, se convierte en la cadena para estas propiedades (y también permanece al principio del **PR_SUBJECT**).</span><span class="sxs-lookup"><span data-stu-id="93a3e-122">If such a substring is found at the beginning of **PR_SUBJECT**, it then becomes the string for these properties (and also stays at the beginning of **PR_SUBJECT**).</span></span> <span data-ttu-id="93a3e-123">De lo contrario, estas propiedades permanecen sin establecer.</span><span class="sxs-lookup"><span data-stu-id="93a3e-123">Otherwise, these properties remain unset.</span></span> 
  
<span data-ttu-id="93a3e-124">Estas propiedades y **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) se deben calcular como parte de la implementación de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="93a3e-124">These properties and **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="93a3e-125">Un cliente no debe solicitar [IMAPIProp::GetProps](imapiprop-getprops.md) para sus valores hasta que se hayan confirmado por una llamada **IMAPIProp::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="93a3e-125">A client should not prompt [IMAPIProp::GetProps](imapiprop-getprops.md) for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="93a3e-126">Las propiedades de asunto son cadenas normalmente pequeñas de menos de 256 caracteres, y un proveedor de almacén de mensajes no está obligado a admitir la interfaz **IStream** OLE en ellos.</span><span class="sxs-lookup"><span data-stu-id="93a3e-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the OLE **IStream** interface on them.</span></span> <span data-ttu-id="93a3e-127">Un cliente siempre debe intentar el acceso a través de la interfaz de **IMAPIProp** en primer lugar y recurrir a **IStream** sólo si se devuelve **MAPI_E_NOT_ENOUGH_MEMORY** .</span><span class="sxs-lookup"><span data-stu-id="93a3e-127">A client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="93a3e-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="93a3e-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="93a3e-129">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="93a3e-129">Protocol specifications</span></span>

<span data-ttu-id="93a3e-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93a3e-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93a3e-131">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="93a3e-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="93a3e-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93a3e-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93a3e-133">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="93a3e-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="93a3e-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93a3e-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93a3e-135">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="93a3e-135">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="93a3e-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="93a3e-136">Header files</span></span>

<span data-ttu-id="93a3e-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="93a3e-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="93a3e-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="93a3e-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="93a3e-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="93a3e-139">Mapitags.h</span></span>
  
> <span data-ttu-id="93a3e-140">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="93a3e-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93a3e-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="93a3e-141">See also</span></span>



[<span data-ttu-id="93a3e-142">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="93a3e-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93a3e-143">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="93a3e-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93a3e-144">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="93a3e-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93a3e-145">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="93a3e-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

