---
title: Propiedad canónico PidTagSendInternetEncoding
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: b6814df2b28961be7e8c07a2d19932988605dc87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820269"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a><span data-ttu-id="45c28-103">Propiedad canónico PidTagSendInternetEncoding</span><span class="sxs-lookup"><span data-stu-id="45c28-103">PidTagSendInternetEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="45c28-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45c28-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45c28-105">Contiene una máscara de bits de codificación preferencias.</span><span class="sxs-lookup"><span data-stu-id="45c28-105">Contains a bitmask of encoding preferences.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45c28-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="45c28-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45c28-107">PR_SEND_INTERNET_ENCODING</span><span class="sxs-lookup"><span data-stu-id="45c28-107">PR_SEND_INTERNET_ENCODING</span></span>  <br/> |
|<span data-ttu-id="45c28-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="45c28-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45c28-109">0x3A71</span><span class="sxs-lookup"><span data-stu-id="45c28-109">0x3A71</span></span>  <br/> |
|<span data-ttu-id="45c28-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="45c28-110">Data type:</span></span>  <br/> |<span data-ttu-id="45c28-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="45c28-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="45c28-112">Área:</span><span class="sxs-lookup"><span data-stu-id="45c28-112">Area:</span></span>  <br/> |<span data-ttu-id="45c28-113">Address</span><span class="sxs-lookup"><span data-stu-id="45c28-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45c28-114">Notas</span><span class="sxs-lookup"><span data-stu-id="45c28-114">Remarks</span></span>

<span data-ttu-id="45c28-115">Establecer esta propiedad para indicar las opciones de codificación utilizadas.</span><span class="sxs-lookup"><span data-stu-id="45c28-115">Set this property to indicate the encoding options used.</span></span> 
  
<span data-ttu-id="45c28-116">Esta propiedad contiene los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="45c28-116">This property contains the following flags:</span></span>
  
<span data-ttu-id="45c28-117">BODY_ENCODING_HTML</span><span class="sxs-lookup"><span data-stu-id="45c28-117">BODY_ENCODING_HTML</span></span> 
  
> <span data-ttu-id="45c28-118">Codificar el texto del mensaje en HTML.</span><span class="sxs-lookup"><span data-stu-id="45c28-118">Encode the message text in HTML.</span></span> <span data-ttu-id="45c28-119">Este indicador se omite a menos que se establece la marca ENCODING_MIME.</span><span class="sxs-lookup"><span data-stu-id="45c28-119">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="45c28-120">BODY_ENCODING_TEXT_AND_HTML</span><span class="sxs-lookup"><span data-stu-id="45c28-120">BODY_ENCODING_TEXT_AND_HTML</span></span> 
  
> <span data-ttu-id="45c28-121">Codificar el texto del mensaje con el texto y el código HTML como alternativas de varias partes de extensiones multipropósito de correo Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="45c28-121">Encode the message text using text and HTML as Multipurpose Internet Mail Extensions (MIME) multipart alternatives.</span></span> <span data-ttu-id="45c28-122">Este indicador se omite a menos que se establece la marca ENCODING_MIME.</span><span class="sxs-lookup"><span data-stu-id="45c28-122">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="45c28-123">ENCODING_MIME</span><span class="sxs-lookup"><span data-stu-id="45c28-123">ENCODING_MIME</span></span> 
  
> <span data-ttu-id="45c28-124">Codificar el mensaje con MIME.</span><span class="sxs-lookup"><span data-stu-id="45c28-124">Encode the message using MIME.</span></span> <span data-ttu-id="45c28-125">Si no se establece este marcador, MAPI codifica el texto del mensaje en texto sin formato y los datos adjuntos de UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="45c28-125">If this flag is not set, MAPI encodes the message text in plain text and the attachments in UUENCODE.</span></span> 
    
<span data-ttu-id="45c28-126">ENCODING_PREFERENCE</span><span class="sxs-lookup"><span data-stu-id="45c28-126">ENCODING_PREFERENCE</span></span> 
  
> <span data-ttu-id="45c28-127">Use los otros marcadores de esta máscara de bits para determinar la codificación.</span><span class="sxs-lookup"><span data-stu-id="45c28-127">Use the other flags in this bitmask to determine the encoding.</span></span> <span data-ttu-id="45c28-128">Si no se establece este marcador, MAPI deja que el sistema de mensajería para tomar decisiones de codificación.</span><span class="sxs-lookup"><span data-stu-id="45c28-128">If this flag is not set, MAPI leaves it to the messaging system to make encoding decisions.</span></span> 
    
<span data-ttu-id="45c28-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span><span class="sxs-lookup"><span data-stu-id="45c28-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span></span> 
  
> <span data-ttu-id="45c28-130">Codificar datos adjuntos de Macintosh en modo doble de Apple.</span><span class="sxs-lookup"><span data-stu-id="45c28-130">Encode Macintosh attachments in Apple double mode.</span></span> <span data-ttu-id="45c28-131">Este indicador se omite a menos que se establece la marca ENCODING_MIME.</span><span class="sxs-lookup"><span data-stu-id="45c28-131">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="45c28-132">MAC_ATTACH_ENCODING_APPLESINGLE</span><span class="sxs-lookup"><span data-stu-id="45c28-132">MAC_ATTACH_ENCODING_APPLESINGLE</span></span> 
  
> <span data-ttu-id="45c28-133">Codificar datos adjuntos de Macintosh en modo simple de Apple.</span><span class="sxs-lookup"><span data-stu-id="45c28-133">Encode Macintosh attachments in Apple single mode.</span></span> <span data-ttu-id="45c28-134">Este indicador se omite a menos que se establece la marca ENCODING_MIME.</span><span class="sxs-lookup"><span data-stu-id="45c28-134">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="45c28-135">MAC_ATTACH_ENCODING_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="45c28-135">MAC_ATTACH_ENCODING_UUENCODE</span></span> 
  
> <span data-ttu-id="45c28-136">Codificar datos adjuntos de Macintosh en UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="45c28-136">Encode Macintosh attachments in UUENCODE.</span></span> <span data-ttu-id="45c28-137">Si se establece la marca ENCODING_MIME, este indicador se omite y codificación BinHex se usa en su lugar.</span><span class="sxs-lookup"><span data-stu-id="45c28-137">If the ENCODING_MIME flag is set, this flag is ignored and BinHex encoding is used instead.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="45c28-138">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="45c28-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45c28-139">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="45c28-139">Protocol specifications</span></span>

<span data-ttu-id="45c28-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45c28-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45c28-141">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="45c28-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45c28-142">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45c28-142">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45c28-143">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="45c28-143">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="45c28-144">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45c28-144">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45c28-145">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="45c28-145">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="45c28-146">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45c28-146">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45c28-147">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="45c28-147">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="45c28-148">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45c28-148">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45c28-149">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="45c28-149">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45c28-150">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="45c28-150">Header files</span></span>

<span data-ttu-id="45c28-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45c28-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="45c28-152">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="45c28-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="45c28-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="45c28-153">Mapitags.h</span></span>
  
> <span data-ttu-id="45c28-154">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="45c28-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45c28-155">Ver también</span><span class="sxs-lookup"><span data-stu-id="45c28-155">See also</span></span>



[<span data-ttu-id="45c28-156">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="45c28-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45c28-157">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="45c28-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45c28-158">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="45c28-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45c28-159">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="45c28-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

