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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342675"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a><span data-ttu-id="7da32-103">Propiedad canónica PidTagSendInternetEncoding</span><span class="sxs-lookup"><span data-stu-id="7da32-103">PidTagSendInternetEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="7da32-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7da32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7da32-105">Contiene una máscara de bits de preferencias de codificación.</span><span class="sxs-lookup"><span data-stu-id="7da32-105">Contains a bitmask of encoding preferences.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7da32-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7da32-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7da32-107">PR_SEND_INTERNET_ENCODING</span><span class="sxs-lookup"><span data-stu-id="7da32-107">PR_SEND_INTERNET_ENCODING</span></span>  <br/> |
|<span data-ttu-id="7da32-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7da32-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7da32-109">0x3A71</span><span class="sxs-lookup"><span data-stu-id="7da32-109">0x3A71</span></span>  <br/> |
|<span data-ttu-id="7da32-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7da32-110">Data type:</span></span>  <br/> |<span data-ttu-id="7da32-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7da32-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7da32-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7da32-112">Area:</span></span>  <br/> |<span data-ttu-id="7da32-113">Address</span><span class="sxs-lookup"><span data-stu-id="7da32-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7da32-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7da32-114">Remarks</span></span>

<span data-ttu-id="7da32-115">Establezca esta propiedad para indicar las opciones de codificación usadas.</span><span class="sxs-lookup"><span data-stu-id="7da32-115">Set this property to indicate the encoding options used.</span></span> 
  
<span data-ttu-id="7da32-116">Esta propiedad contiene las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="7da32-116">This property contains the following flags:</span></span>
  
<span data-ttu-id="7da32-117">BODY_ENCODING_HTML</span><span class="sxs-lookup"><span data-stu-id="7da32-117">BODY_ENCODING_HTML</span></span> 
  
> <span data-ttu-id="7da32-118">Codifica el texto del mensaje en HTML.</span><span class="sxs-lookup"><span data-stu-id="7da32-118">Encode the message text in HTML.</span></span> <span data-ttu-id="7da32-119">Esta marca se omite a menos que ENCODING_MIME esté establecida.</span><span class="sxs-lookup"><span data-stu-id="7da32-119">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="7da32-120">BODY_ENCODING_TEXT_AND_HTML</span><span class="sxs-lookup"><span data-stu-id="7da32-120">BODY_ENCODING_TEXT_AND_HTML</span></span> 
  
> <span data-ttu-id="7da32-121">Codificar el texto del mensaje con texto y HTML como alternativas multipart extensions multipropósito al correo de Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="7da32-121">Encode the message text using text and HTML as Multipurpose Internet Mail Extensions (MIME) multipart alternatives.</span></span> <span data-ttu-id="7da32-122">Esta marca se omite a menos que ENCODING_MIME esté establecida.</span><span class="sxs-lookup"><span data-stu-id="7da32-122">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="7da32-123">ENCODING_MIME</span><span class="sxs-lookup"><span data-stu-id="7da32-123">ENCODING_MIME</span></span> 
  
> <span data-ttu-id="7da32-124">Codifica el mensaje con MIME.</span><span class="sxs-lookup"><span data-stu-id="7da32-124">Encode the message using MIME.</span></span> <span data-ttu-id="7da32-125">Si no se establece esta marca, MAPI codifica el texto del mensaje en texto sin formato y los datos adjuntos en UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="7da32-125">If this flag is not set, MAPI encodes the message text in plain text and the attachments in UUENCODE.</span></span> 
    
<span data-ttu-id="7da32-126">ENCODING_PREFERENCE</span><span class="sxs-lookup"><span data-stu-id="7da32-126">ENCODING_PREFERENCE</span></span> 
  
> <span data-ttu-id="7da32-127">Use las otras marcas de esta máscara de bits para determinar la codificación.</span><span class="sxs-lookup"><span data-stu-id="7da32-127">Use the other flags in this bitmask to determine the encoding.</span></span> <span data-ttu-id="7da32-128">Si no se establece esta marca, MAPI la deja en el sistema de mensajería para tomar decisiones de codificación.</span><span class="sxs-lookup"><span data-stu-id="7da32-128">If this flag is not set, MAPI leaves it to the messaging system to make encoding decisions.</span></span> 
    
<span data-ttu-id="7da32-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span><span class="sxs-lookup"><span data-stu-id="7da32-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span></span> 
  
> <span data-ttu-id="7da32-130">Codificar datos adjuntos de Macintosh en modo doble de Apple.</span><span class="sxs-lookup"><span data-stu-id="7da32-130">Encode Macintosh attachments in Apple double mode.</span></span> <span data-ttu-id="7da32-131">Esta marca se omite a menos que ENCODING_MIME esté establecida.</span><span class="sxs-lookup"><span data-stu-id="7da32-131">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="7da32-132">MAC_ATTACH_ENCODING_APPLESINGLE</span><span class="sxs-lookup"><span data-stu-id="7da32-132">MAC_ATTACH_ENCODING_APPLESINGLE</span></span> 
  
> <span data-ttu-id="7da32-133">Codificar datos adjuntos de Macintosh en modo único de Apple.</span><span class="sxs-lookup"><span data-stu-id="7da32-133">Encode Macintosh attachments in Apple single mode.</span></span> <span data-ttu-id="7da32-134">Esta marca se omite a menos que ENCODING_MIME esté establecida.</span><span class="sxs-lookup"><span data-stu-id="7da32-134">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="7da32-135">MAC_ATTACH_ENCODING_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="7da32-135">MAC_ATTACH_ENCODING_UUENCODE</span></span> 
  
> <span data-ttu-id="7da32-136">Codificar datos adjuntos de Macintosh en UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="7da32-136">Encode Macintosh attachments in UUENCODE.</span></span> <span data-ttu-id="7da32-137">Si se ENCODING_MIME marca predeterminada, esta marca se omite y se usa la codificación BinHex en su lugar.</span><span class="sxs-lookup"><span data-stu-id="7da32-137">If the ENCODING_MIME flag is set, this flag is ignored and BinHex encoding is used instead.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="7da32-138">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7da32-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7da32-139">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="7da32-139">Protocol specifications</span></span>

<span data-ttu-id="7da32-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7da32-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7da32-141">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="7da32-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7da32-142">[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7da32-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7da32-143">Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="7da32-143">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="7da32-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7da32-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7da32-145">Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="7da32-145">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="7da32-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7da32-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7da32-147">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7da32-147">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="7da32-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7da32-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7da32-149">Especifica las propiedades y las operaciones permitidas para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="7da32-149">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7da32-150">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7da32-150">Header files</span></span>

<span data-ttu-id="7da32-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7da32-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="7da32-152">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7da32-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="7da32-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7da32-153">Mapitags.h</span></span>
  
> <span data-ttu-id="7da32-154">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="7da32-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7da32-155">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7da32-155">See also</span></span>



[<span data-ttu-id="7da32-156">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7da32-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7da32-157">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="7da32-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7da32-158">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7da32-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7da32-159">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="7da32-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

