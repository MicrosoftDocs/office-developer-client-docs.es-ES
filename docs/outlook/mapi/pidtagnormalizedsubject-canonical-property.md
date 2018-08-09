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
ms.openlocfilehash: 74061f33a88dceb371cad00ef44f611b583f7ae2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819780"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a><span data-ttu-id="5229a-103">Propiedad canónica PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="5229a-103">PidTagNormalizedSubject Canonical Property</span></span>

  
  
<span data-ttu-id="5229a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5229a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5229a-105">Contiene al asunto del mensaje con cualquier prefijo que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="5229a-105">Contains the message subject with any prefix removed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5229a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5229a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5229a-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="5229a-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="5229a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5229a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5229a-109">0x0E1D</span><span class="sxs-lookup"><span data-stu-id="5229a-109">0x0E1D</span></span>  <br/> |
|<span data-ttu-id="5229a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5229a-110">Data type:</span></span>  <br/> |<span data-ttu-id="5229a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5229a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5229a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5229a-112">Area:</span></span>  <br/> |<span data-ttu-id="5229a-113">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="5229a-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5229a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5229a-114">Remarks</span></span>

<span data-ttu-id="5229a-115">Estas propiedades se calculan por almacén de mensajes o los proveedores de las propiedades de **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) y **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) de transporte de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="5229a-115">These properties are computed by message store or transport providers from the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties in the following manner.</span></span>
  
- <span data-ttu-id="5229a-116">Si el **PR_SUBJECT_PREFIX** está presente y es una subcadena inicial de **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** y las propiedades asociadas se establecen en el contenido de **PR_SUBJECT** con el prefijo que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="5229a-116">If the **PR_SUBJECT_PREFIX** is present and is an initial substring of **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** and associated properties are set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
- <span data-ttu-id="5229a-117">Si **PR_SUBJECT_PREFIX** está presente, pero no es una subcadena inicial de **PR_SUBJECT**, **PR_SUBJECT_PREFIX** se elimina y se vuelve a calcular desde **PR_SUBJECT** utilizando la siguiente regla: si la cadena contenida en **PR_SUBJECT** se comienza con uno a tres caracteres no numéricos, seguidos de un punto y coma y un espacio, a continuación, la cadena junto con los dos puntos y el espacio en blanco se convierte en el prefijo.</span><span class="sxs-lookup"><span data-stu-id="5229a-117">If **PR_SUBJECT_PREFIX** is present, but it is not an initial substring of **PR_SUBJECT**, **PR_SUBJECT_PREFIX** is deleted and recalculated from **PR_SUBJECT** using the following rule: If the string contained in **PR_SUBJECT** begins with one to three non-numeric characters followed by a colon and a space, then the string together with the colon and the blank becomes the prefix.</span></span> <span data-ttu-id="5229a-118">Caracteres de números, espacios y signos de puntuación no son caracteres de prefijo válido.</span><span class="sxs-lookup"><span data-stu-id="5229a-118">Numbers, blanks, and punctuation characters are not valid prefix characters.</span></span> 
    
- <span data-ttu-id="5229a-119">Si **PR_SUBJECT_PREFIX** no está presente, se calcula a partir **PR_SUBJECT** utilizando la regla que se describen en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="5229a-119">If **PR_SUBJECT_PREFIX** is not present, it is calculated from **PR_SUBJECT** using the rule outlined in the previous step.</span></span> <span data-ttu-id="5229a-120">Esta propiedad, a continuación, se establece en el contenido de **PR_SUBJECT** con el prefijo que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="5229a-120">This property then is set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
 <span data-ttu-id="5229a-121">**Nota** Cuando **PR_SUBJECT_PREFIX** es una cadena vacía, **PR_SUBJECT** y esta propiedad son los mismos.</span><span class="sxs-lookup"><span data-stu-id="5229a-121">**Note** When **PR_SUBJECT_PREFIX** is an empty string, **PR_SUBJECT** and this property are the same.</span></span> 
  
<span data-ttu-id="5229a-122">En última instancia, esta propiedad debe ser la parte de **PR_SUBJECT** siguiendo el prefijo.</span><span class="sxs-lookup"><span data-stu-id="5229a-122">Ultimately, this property should be the part of **PR_SUBJECT** following the prefix.</span></span> <span data-ttu-id="5229a-123">Si no hay ningún prefijo, esta propiedad se convierte en el mismo como **PR_SUBJECT**.</span><span class="sxs-lookup"><span data-stu-id="5229a-123">If there is no prefix, this property becomes the same as **PR_SUBJECT**.</span></span>
  
 <span data-ttu-id="5229a-124">**PR_SUBJECT_PREFIX** y esta propiedad se deben calcular como parte de la implementación de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="5229a-124">**PR_SUBJECT_PREFIX** and this property should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="5229a-125">Una aplicación de cliente no debe solicitar el método [IMAPIProp::GetProps](imapiprop-getprops.md) para sus valores hasta que se hayan confirmado por una llamada **IMAPIProp::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="5229a-125">A client application should not prompt the [IMAPIProp::GetProps](imapiprop-getprops.md) method for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="5229a-126">Las propiedades de asunto son cadenas normalmente pequeñas de menos de 256 caracteres, y un proveedor de almacén de mensajes no está obligado a compatible con la interfaz de vinculación e incrustación de objetos (OLE) **IStream** en ellos.</span><span class="sxs-lookup"><span data-stu-id="5229a-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="5229a-127">El cliente siempre debe intentar el acceso a través de la interfaz de **IMAPIProp** en primer lugar y recurrir a **IStream** sólo si se devuelve MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="5229a-127">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if MAPI_E_NOT_ENOUGH_MEMORY is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5229a-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5229a-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5229a-129">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5229a-129">Protocol specifications</span></span>

<span data-ttu-id="5229a-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5229a-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5229a-131">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5229a-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5229a-132">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5229a-132">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5229a-133">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="5229a-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="5229a-134">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5229a-134">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5229a-135">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="5229a-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5229a-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5229a-136">Header files</span></span>

<span data-ttu-id="5229a-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5229a-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="5229a-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5229a-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="5229a-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5229a-139">Mapitags.h</span></span>
  
> <span data-ttu-id="5229a-140">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="5229a-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5229a-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="5229a-141">See also</span></span>



[<span data-ttu-id="5229a-142">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5229a-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5229a-143">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5229a-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5229a-144">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5229a-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5229a-145">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5229a-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

