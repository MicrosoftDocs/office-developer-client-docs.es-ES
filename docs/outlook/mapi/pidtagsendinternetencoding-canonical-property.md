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
ms.openlocfilehash: e157fa640026d13362084b30ad73cdb66a0b35b5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392574"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a><span data-ttu-id="0b312-103">Propiedad canónica PidTagSendInternetEncoding</span><span class="sxs-lookup"><span data-stu-id="0b312-103">PidTagSendInternetEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="0b312-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b312-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b312-105">Contiene una máscara de bits de codificación preferencias.</span><span class="sxs-lookup"><span data-stu-id="0b312-105">Contains a bitmask of encoding preferences.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b312-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0b312-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b312-107">PR_SEND_INTERNET_ENCODING</span><span class="sxs-lookup"><span data-stu-id="0b312-107">PR_SEND_INTERNET_ENCODING</span></span>  <br/> |
|<span data-ttu-id="0b312-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0b312-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0b312-109">0x3A71</span><span class="sxs-lookup"><span data-stu-id="0b312-109">0x3A71</span></span>  <br/> |
|<span data-ttu-id="0b312-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0b312-110">Data type:</span></span>  <br/> |<span data-ttu-id="0b312-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0b312-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0b312-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0b312-112">Area:</span></span>  <br/> |<span data-ttu-id="0b312-113">Address</span><span class="sxs-lookup"><span data-stu-id="0b312-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b312-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0b312-114">Remarks</span></span>

<span data-ttu-id="0b312-115">Establecer esta propiedad para indicar las opciones de codificación utilizadas.</span><span class="sxs-lookup"><span data-stu-id="0b312-115">Set this property to indicate the encoding options used.</span></span> 
  
<span data-ttu-id="0b312-116">Esta propiedad contiene los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="0b312-116">This property contains the following flags:</span></span>
  
<span data-ttu-id="0b312-117">BODY_ENCODING_HTML</span><span class="sxs-lookup"><span data-stu-id="0b312-117">BODY_ENCODING_HTML</span></span> 
  
> <span data-ttu-id="0b312-118">Codificar el texto del mensaje en HTML.</span><span class="sxs-lookup"><span data-stu-id="0b312-118">Encode the message text in HTML.</span></span> <span data-ttu-id="0b312-119">Este indicador se omite a menos que se establece la marca ENCODING_MIME.</span><span class="sxs-lookup"><span data-stu-id="0b312-119">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="0b312-120">BODY_ENCODING_TEXT_AND_HTML</span><span class="sxs-lookup"><span data-stu-id="0b312-120">BODY_ENCODING_TEXT_AND_HTML</span></span> 
  
> <span data-ttu-id="0b312-121">Codificar el texto del mensaje con el texto y el código HTML como alternativas de varias partes de extensiones multipropósito de correo Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="0b312-121">Encode the message text using text and HTML as Multipurpose Internet Mail Extensions (MIME) multipart alternatives.</span></span> <span data-ttu-id="0b312-122">Este indicador se omite a menos que se establece la marca ENCODING_MIME.</span><span class="sxs-lookup"><span data-stu-id="0b312-122">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="0b312-123">ENCODING_MIME</span><span class="sxs-lookup"><span data-stu-id="0b312-123">ENCODING_MIME</span></span> 
  
> <span data-ttu-id="0b312-124">Codificar el mensaje con MIME.</span><span class="sxs-lookup"><span data-stu-id="0b312-124">Encode the message using MIME.</span></span> <span data-ttu-id="0b312-125">Si no se establece este marcador, MAPI codifica el texto del mensaje en texto sin formato y los datos adjuntos de UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="0b312-125">If this flag is not set, MAPI encodes the message text in plain text and the attachments in UUENCODE.</span></span> 
    
<span data-ttu-id="0b312-126">ENCODING_PREFERENCE</span><span class="sxs-lookup"><span data-stu-id="0b312-126">ENCODING_PREFERENCE</span></span> 
  
> <span data-ttu-id="0b312-127">Use los otros marcadores de esta máscara de bits para determinar la codificación.</span><span class="sxs-lookup"><span data-stu-id="0b312-127">Use the other flags in this bitmask to determine the encoding.</span></span> <span data-ttu-id="0b312-128">Si no se establece este marcador, MAPI deja que el sistema de mensajería para tomar decisiones de codificación.</span><span class="sxs-lookup"><span data-stu-id="0b312-128">If this flag is not set, MAPI leaves it to the messaging system to make encoding decisions.</span></span> 
    
<span data-ttu-id="0b312-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span><span class="sxs-lookup"><span data-stu-id="0b312-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span></span> 
  
> <span data-ttu-id="0b312-130">Codificar datos adjuntos de Macintosh en modo doble de Apple.</span><span class="sxs-lookup"><span data-stu-id="0b312-130">Encode Macintosh attachments in Apple double mode.</span></span> <span data-ttu-id="0b312-131">Este indicador se omite a menos que se establece la marca ENCODING_MIME.</span><span class="sxs-lookup"><span data-stu-id="0b312-131">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="0b312-132">MAC_ATTACH_ENCODING_APPLESINGLE</span><span class="sxs-lookup"><span data-stu-id="0b312-132">MAC_ATTACH_ENCODING_APPLESINGLE</span></span> 
  
> <span data-ttu-id="0b312-133">Codificar datos adjuntos de Macintosh en modo simple de Apple.</span><span class="sxs-lookup"><span data-stu-id="0b312-133">Encode Macintosh attachments in Apple single mode.</span></span> <span data-ttu-id="0b312-134">Este indicador se omite a menos que se establece la marca ENCODING_MIME.</span><span class="sxs-lookup"><span data-stu-id="0b312-134">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="0b312-135">MAC_ATTACH_ENCODING_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="0b312-135">MAC_ATTACH_ENCODING_UUENCODE</span></span> 
  
> <span data-ttu-id="0b312-136">Codificar datos adjuntos de Macintosh en UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="0b312-136">Encode Macintosh attachments in UUENCODE.</span></span> <span data-ttu-id="0b312-137">Si se establece la marca ENCODING_MIME, este indicador se omite y codificación BinHex se usa en su lugar.</span><span class="sxs-lookup"><span data-stu-id="0b312-137">If the ENCODING_MIME flag is set, this flag is ignored and BinHex encoding is used instead.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="0b312-138">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b312-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0b312-139">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0b312-139">Protocol specifications</span></span>

<span data-ttu-id="0b312-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b312-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b312-141">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0b312-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0b312-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b312-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b312-143">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="0b312-143">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="0b312-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b312-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b312-145">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="0b312-145">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="0b312-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b312-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b312-147">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0b312-147">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="0b312-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b312-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b312-149">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="0b312-149">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0b312-150">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0b312-150">Header files</span></span>

<span data-ttu-id="0b312-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b312-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b312-152">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0b312-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="0b312-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0b312-153">Mapitags.h</span></span>
  
> <span data-ttu-id="0b312-154">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="0b312-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b312-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b312-155">See also</span></span>



[<span data-ttu-id="0b312-156">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0b312-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b312-157">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0b312-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b312-158">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0b312-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b312-159">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="0b312-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

