---
title: Propiedad canónica PidTagNormalizedSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 54a0f438dacc8a1c7838eb538ec05c5c263f1b0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329277"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a><span data-ttu-id="93a51-103">Propiedad canónica PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="93a51-103">PidTagNormalizedSubject Canonical Property</span></span>

  
  
<span data-ttu-id="93a51-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93a51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93a51-105">Contiene el asunto del mensaje con cualquier prefijo eliminado.</span><span class="sxs-lookup"><span data-stu-id="93a51-105">Contains the message subject with any prefix removed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93a51-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="93a51-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93a51-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="93a51-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="93a51-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="93a51-108">Identifier:</span></span>  <br/> |<span data-ttu-id="93a51-109">0x0E1D</span><span class="sxs-lookup"><span data-stu-id="93a51-109">0x0E1D</span></span>  <br/> |
|<span data-ttu-id="93a51-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="93a51-110">Data type:</span></span>  <br/> |<span data-ttu-id="93a51-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="93a51-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="93a51-112">Área:</span><span class="sxs-lookup"><span data-stu-id="93a51-112">Area:</span></span>  <br/> |<span data-ttu-id="93a51-113">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="93a51-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93a51-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="93a51-114">Remarks</span></span>

<span data-ttu-id="93a51-115">Estas propiedades son calculadas por los proveedores de almacenamiento de mensajes o transporte desde las propiedades **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) y **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="93a51-115">These properties are computed by message store or transport providers from the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties in the following manner.</span></span>
  
- <span data-ttu-id="93a51-116">Si **PR_SUBJECT_PREFIX** está presente y es una subcadena inicial de **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** y las propiedades asociadas se establecen en el contenido de **PR_SUBJECT** con el prefijo quitado.</span><span class="sxs-lookup"><span data-stu-id="93a51-116">If the **PR_SUBJECT_PREFIX** is present and is an initial substring of **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** and associated properties are set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
- <span data-ttu-id="93a51-117">Si **PR_SUBJECT_PREFIX** está presente, pero no es una subcadena inicial de **PR_SUBJECT**, **PR_SUBJECT_PREFIX** se elimina y se vuelve a calcular desde **PR_SUBJECT** con la siguiente regla: Si la cadena contenida en **PR_SUBJECT** empieza con uno o tres caracteres no numéricos seguidos de dos puntos y un espacio, la cadena junto con los dos puntos y el espacio en blanco se convierten en el prefijo.</span><span class="sxs-lookup"><span data-stu-id="93a51-117">If **PR_SUBJECT_PREFIX** is present, but it is not an initial substring of **PR_SUBJECT**, **PR_SUBJECT_PREFIX** is deleted and recalculated from **PR_SUBJECT** using the following rule: If the string contained in **PR_SUBJECT** begins with one to three non-numeric characters followed by a colon and a space, then the string together with the colon and the blank becomes the prefix.</span></span> <span data-ttu-id="93a51-118">Los números, los espacios en blanco y los caracteres de puntuación no son caracteres de prefijo válidos.</span><span class="sxs-lookup"><span data-stu-id="93a51-118">Numbers, blanks, and punctuation characters are not valid prefix characters.</span></span> 
    
- <span data-ttu-id="93a51-119">Si **PR_SUBJECT_PREFIX** no está presente, se calcula a partir de **PR_SUBJECT** mediante la regla que se describe en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="93a51-119">If **PR_SUBJECT_PREFIX** is not present, it is calculated from **PR_SUBJECT** using the rule outlined in the previous step.</span></span> <span data-ttu-id="93a51-120">Esta propiedad se establece en el contenido de **PR_SUBJECT** con el prefijo quitado.</span><span class="sxs-lookup"><span data-stu-id="93a51-120">This property then is set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
 <span data-ttu-id="93a51-121">**Nota:** Cuando **PR_SUBJECT_PREFIX** es una cadena vacía, **PR_SUBJECT** y esta propiedad son iguales.</span><span class="sxs-lookup"><span data-stu-id="93a51-121">**Note** When **PR_SUBJECT_PREFIX** is an empty string, **PR_SUBJECT** and this property are the same.</span></span> 
  
<span data-ttu-id="93a51-122">En última instancia, esta propiedad debe ser la parte de **PR_SUBJECT** después del prefijo.</span><span class="sxs-lookup"><span data-stu-id="93a51-122">Ultimately, this property should be the part of **PR_SUBJECT** following the prefix.</span></span> <span data-ttu-id="93a51-123">Si no hay prefijo, esta propiedad pasa a ser la misma que **PR_SUBJECT**.</span><span class="sxs-lookup"><span data-stu-id="93a51-123">If there is no prefix, this property becomes the same as **PR_SUBJECT**.</span></span>
  
 <span data-ttu-id="93a51-124">**PR_SUBJECT_PREFIX** y esta propiedad se deben calcular como parte de la implementación de [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="93a51-124">**PR_SUBJECT_PREFIX** and this property should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="93a51-125">Una aplicación cliente no debe solicitar el método [IMAPIProp:: GetProps](imapiprop-getprops.md) para sus valores hasta que haya sido confirmada por una llamada a **IMAPIProp:: SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="93a51-125">A client application should not prompt the [IMAPIProp::GetProps](imapiprop-getprops.md) method for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="93a51-126">Las propiedades de asunto suelen ser cadenas pequeñas de menos de 256 caracteres y un proveedor de almacenamiento de mensajes no está obligado a admitir la interfaz **IStream** de vinculación e incrustación de objetos (OLE) en ellas.</span><span class="sxs-lookup"><span data-stu-id="93a51-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="93a51-127">El cliente siempre debe intentar obtener acceso a través de la interfaz **IMAPIProp** en primer lugar y recurrir a **IStream** solo si se devuelve MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="93a51-127">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if MAPI_E_NOT_ENOUGH_MEMORY is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="93a51-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="93a51-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="93a51-129">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="93a51-129">Protocol specifications</span></span>

<span data-ttu-id="93a51-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93a51-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93a51-131">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="93a51-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="93a51-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93a51-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93a51-133">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="93a51-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="93a51-134">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93a51-134">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93a51-135">Especifica las propiedades y operaciones que se admiten para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="93a51-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="93a51-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="93a51-136">Header files</span></span>

<span data-ttu-id="93a51-137">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="93a51-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="93a51-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="93a51-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="93a51-139">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="93a51-139">Mapitags.h</span></span>
  
> <span data-ttu-id="93a51-140">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="93a51-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93a51-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="93a51-141">See also</span></span>



[<span data-ttu-id="93a51-142">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="93a51-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93a51-143">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="93a51-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93a51-144">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="93a51-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93a51-145">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="93a51-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

