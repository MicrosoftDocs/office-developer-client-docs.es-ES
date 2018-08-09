---
title: Propiedad canónica PidTagSendInternetEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendInternetEncoding
api_type:
- COM
ms.assetid: ae408b4f-dee3-484b-a19c-f472cfa95996
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b6814df2b28961be7e8c07a2d19932988605dc87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820269"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a><span data-ttu-id="72ced-103">Propiedad canónica PidTagSendInternetEncoding</span><span class="sxs-lookup"><span data-stu-id="72ced-103">PidTagSendInternetEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="72ced-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72ced-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72ced-105">Contiene una máscara de bits de codificación preferencias.</span><span class="sxs-lookup"><span data-stu-id="72ced-105">Contains a bitmask of encoding preferences.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72ced-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="72ced-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="72ced-107">PR_SEND_INTERNET_ENCODING</span><span class="sxs-lookup"><span data-stu-id="72ced-107">PR_SEND_INTERNET_ENCODING</span></span>  <br/> |
|<span data-ttu-id="72ced-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="72ced-108">Identifier:</span></span>  <br/> |<span data-ttu-id="72ced-109">0x3A71</span><span class="sxs-lookup"><span data-stu-id="72ced-109">0x3A71</span></span>  <br/> |
|<span data-ttu-id="72ced-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="72ced-110">Data type:</span></span>  <br/> |<span data-ttu-id="72ced-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="72ced-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="72ced-112">Área:</span><span class="sxs-lookup"><span data-stu-id="72ced-112">Area:</span></span>  <br/> |<span data-ttu-id="72ced-113">Address</span><span class="sxs-lookup"><span data-stu-id="72ced-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72ced-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="72ced-114">Remarks</span></span>

<span data-ttu-id="72ced-115">Establecer esta propiedad para indicar las opciones de codificación utilizadas.</span><span class="sxs-lookup"><span data-stu-id="72ced-115">Set this property to indicate the encoding options used.</span></span> 
  
<span data-ttu-id="72ced-116">Esta propiedad contiene los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="72ced-116">This property contains the following flags:</span></span>
  
<span data-ttu-id="72ced-117">BODY_ENCODING_HTML</span><span class="sxs-lookup"><span data-stu-id="72ced-117">BODY_ENCODING_HTML</span></span> 
  
> <span data-ttu-id="72ced-118">Codificar el texto del mensaje en HTML.</span><span class="sxs-lookup"><span data-stu-id="72ced-118">Encode the message text in HTML.</span></span> <span data-ttu-id="72ced-119">Este indicador se omite a menos que se establece la marca ENCODING_MIME.</span><span class="sxs-lookup"><span data-stu-id="72ced-119">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="72ced-120">BODY_ENCODING_TEXT_AND_HTML</span><span class="sxs-lookup"><span data-stu-id="72ced-120">BODY_ENCODING_TEXT_AND_HTML</span></span> 
  
> <span data-ttu-id="72ced-121">Codificar el texto del mensaje con el texto y el código HTML como alternativas de varias partes de extensiones multipropósito de correo Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="72ced-121">Encode the message text using text and HTML as Multipurpose Internet Mail Extensions (MIME) multipart alternatives.</span></span> <span data-ttu-id="72ced-122">Este indicador se omite a menos que se establece la marca ENCODING_MIME.</span><span class="sxs-lookup"><span data-stu-id="72ced-122">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="72ced-123">ENCODING_MIME</span><span class="sxs-lookup"><span data-stu-id="72ced-123">ENCODING_MIME</span></span> 
  
> <span data-ttu-id="72ced-124">Codificar el mensaje con MIME.</span><span class="sxs-lookup"><span data-stu-id="72ced-124">Encode the message using MIME.</span></span> <span data-ttu-id="72ced-125">Si no se establece este marcador, MAPI codifica el texto del mensaje en texto sin formato y los datos adjuntos de UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="72ced-125">If this flag is not set, MAPI encodes the message text in plain text and the attachments in UUENCODE.</span></span> 
    
<span data-ttu-id="72ced-126">ENCODING_PREFERENCE</span><span class="sxs-lookup"><span data-stu-id="72ced-126">ENCODING_PREFERENCE</span></span> 
  
> <span data-ttu-id="72ced-127">Use los otros marcadores de esta máscara de bits para determinar la codificación.</span><span class="sxs-lookup"><span data-stu-id="72ced-127">Use the other flags in this bitmask to determine the encoding.</span></span> <span data-ttu-id="72ced-128">Si no se establece este marcador, MAPI deja que el sistema de mensajería para tomar decisiones de codificación.</span><span class="sxs-lookup"><span data-stu-id="72ced-128">If this flag is not set, MAPI leaves it to the messaging system to make encoding decisions.</span></span> 
    
<span data-ttu-id="72ced-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span><span class="sxs-lookup"><span data-stu-id="72ced-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span></span> 
  
> <span data-ttu-id="72ced-130">Codificar datos adjuntos de Macintosh en modo doble de Apple.</span><span class="sxs-lookup"><span data-stu-id="72ced-130">Encode Macintosh attachments in Apple double mode.</span></span> <span data-ttu-id="72ced-131">Este indicador se omite a menos que se establece la marca ENCODING_MIME.</span><span class="sxs-lookup"><span data-stu-id="72ced-131">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="72ced-132">MAC_ATTACH_ENCODING_APPLESINGLE</span><span class="sxs-lookup"><span data-stu-id="72ced-132">MAC_ATTACH_ENCODING_APPLESINGLE</span></span> 
  
> <span data-ttu-id="72ced-133">Codificar datos adjuntos de Macintosh en modo simple de Apple.</span><span class="sxs-lookup"><span data-stu-id="72ced-133">Encode Macintosh attachments in Apple single mode.</span></span> <span data-ttu-id="72ced-134">Este indicador se omite a menos que se establece la marca ENCODING_MIME.</span><span class="sxs-lookup"><span data-stu-id="72ced-134">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="72ced-135">MAC_ATTACH_ENCODING_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="72ced-135">MAC_ATTACH_ENCODING_UUENCODE</span></span> 
  
> <span data-ttu-id="72ced-136">Codificar datos adjuntos de Macintosh en UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="72ced-136">Encode Macintosh attachments in UUENCODE.</span></span> <span data-ttu-id="72ced-137">Si se establece la marca ENCODING_MIME, este indicador se omite y codificación BinHex se usa en su lugar.</span><span class="sxs-lookup"><span data-stu-id="72ced-137">If the ENCODING_MIME flag is set, this flag is ignored and BinHex encoding is used instead.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="72ced-138">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="72ced-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="72ced-139">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="72ced-139">Protocol specifications</span></span>

<span data-ttu-id="72ced-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72ced-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72ced-141">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="72ced-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="72ced-142">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72ced-142">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72ced-143">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="72ced-143">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="72ced-144">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72ced-144">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72ced-145">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="72ced-145">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="72ced-146">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72ced-146">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72ced-147">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="72ced-147">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="72ced-148">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72ced-148">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72ced-149">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="72ced-149">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="72ced-150">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="72ced-150">Header files</span></span>

<span data-ttu-id="72ced-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="72ced-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="72ced-152">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="72ced-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="72ced-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="72ced-153">Mapitags.h</span></span>
  
> <span data-ttu-id="72ced-154">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="72ced-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72ced-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="72ced-155">See also</span></span>



[<span data-ttu-id="72ced-156">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="72ced-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="72ced-157">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="72ced-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="72ced-158">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="72ced-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="72ced-159">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="72ced-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

