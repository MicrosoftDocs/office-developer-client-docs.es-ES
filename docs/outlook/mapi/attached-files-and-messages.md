---
title: Archivos y mensajes adjuntos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b2f2fb72-23ae-4e0b-a8a1-3b78a1862acb
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c4dbe1a761a753bef77168aec8d2674a1b2b100e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436842"
---
# <a name="attached-files-and-messages"></a><span data-ttu-id="acc5c-103">Archivos y mensajes adjuntos</span><span class="sxs-lookup"><span data-stu-id="acc5c-103">Attached Files and Messages</span></span>

  
  
<span data-ttu-id="acc5c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acc5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acc5c-105">Si se usa MIME con TNEF al codificar el contenido del mensaje, todas las propiedades de datos adjuntos y el contenido se encuentran en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="acc5c-105">If MIME with TNEF is used while encoding message content,all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="acc5c-106">El TNEF en sí es un único archivo adjunto binario denominado Winmail.dat, codificado como se describe para MIME sin TNEF.</span><span class="sxs-lookup"><span data-stu-id="acc5c-106">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for MIME without TNEF.</span></span> 
  
<span data-ttu-id="acc5c-107">Si se usa MIME sin TNEF, los archivos adjuntos se envían como elementos de contenido de mensajes MIME.</span><span class="sxs-lookup"><span data-stu-id="acc5c-107">If MIME is used without TNEF, attached files are sent as MIME message content parts.</span></span> <span data-ttu-id="acc5c-108">El nombre de archivo se coloca en el  *parámetro name*  en el  *encabezado Content-type*  para los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="acc5c-108">The filename is placed in the  *name*  parameter to the  *Content-type*  header for the attachment.</span></span> <span data-ttu-id="acc5c-109">El juego de caracteres para los datos adjuntos se coloca en el  *parámetro charset*  al  *tipo Content*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content.</span><span class="sxs-lookup"><span data-stu-id="acc5c-109">The character set for the attachment is placed in the  *charset*  parameter to the  *Content-type*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content.</span></span> <span data-ttu-id="acc5c-110">Los datos adjuntos de dirección URL se tratan especialmente:</span><span class="sxs-lookup"><span data-stu-id="acc5c-110">URL attachments are treated specially:</span></span> 
  
- <span data-ttu-id="acc5c-111">Si los datos adjuntos son una dirección URL (un archivo adjunto con extensión . URL), y el modo de acceso definido en él es FTP anónimo, se codifica como un mensaje externo y el contenido del archivo (la dirección URL) se copia en el encabezado del mensaje externo.</span><span class="sxs-lookup"><span data-stu-id="acc5c-111">If the attachment is a URL (an attached file with extension .URL), and the access mode defined in it is anonymous FTP, it is encoded as an external message, and the content of the file (the URL) is copied into the header of the external message.</span></span> <span data-ttu-id="acc5c-112">*Tipo de contenido: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bits se supone).</span><span class="sxs-lookup"><span data-stu-id="acc5c-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span></span> 
    
- <span data-ttu-id="acc5c-113">Si solo se encuentran caracteres de 7 bits y ninguna línea supera los 140 caracteres de longitud, los datos adjuntos son texto ASCII.</span><span class="sxs-lookup"><span data-stu-id="acc5c-113">If only 7-bit characters are found and no line exceeds 140 characters in length, the attachment is ASCII text.</span></span> <span data-ttu-id="acc5c-114">*Tipo de contenido: texto/sin formato; charset=us-ascii Content-Transfer-Encoding: 7bits*</span><span class="sxs-lookup"><span data-stu-id="acc5c-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span></span> 
    
- <span data-ttu-id="acc5c-115">Si se encuentran líneas largas o hasta un 25 % de caracteres de 8 bits, el contenido de los datos adjuntos es texto y el juego de caracteres lo determina la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="acc5c-115">If long lines or up to 25% 8-bit characters are found, the attachment content is text and the character set is determined by the locale.</span></span> <span data-ttu-id="acc5c-116">Debe elegirse entre los conjuntos de caracteres definidos por la norma ISO 8859.</span><span class="sxs-lookup"><span data-stu-id="acc5c-116">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="acc5c-117">*Tipo de contenido: texto/sin formato; charset=ISO-8859-1*  (por ejemplo)</span><span class="sxs-lookup"><span data-stu-id="acc5c-117">*Content-type: text/plain; charset=ISO-8859-1*  (for example)</span></span> 
    
     <span data-ttu-id="acc5c-118">*Content-Transfer-Encoding: quoted-printable*</span><span class="sxs-lookup"><span data-stu-id="acc5c-118">*Content-Transfer-Encoding: quoted-printable*</span></span> 
    
- <span data-ttu-id="acc5c-119">Si el 25 % o más de los caracteres tienen el conjunto de bits alto, los datos adjuntos son binarios.</span><span class="sxs-lookup"><span data-stu-id="acc5c-119">If 25% or more of the characters have the high bit set, the attachment is binary.</span></span> <span data-ttu-id="acc5c-120">Se codifica mediante el algoritmo Base64.</span><span class="sxs-lookup"><span data-stu-id="acc5c-120">It is encoded using the Base64 algorithm.</span></span> <span data-ttu-id="acc5c-121">*Tipo de contenido: application/octet-stream*  (de forma predeterminada, en función de la extensión de archivo)</span><span class="sxs-lookup"><span data-stu-id="acc5c-121">*Content-type: application/octet-stream*  (by default; based on file extension)</span></span> 
    
     * <span data-ttu-id="acc5c-122">Content-Transfer-Encoding: base64 \*</span><span class="sxs-lookup"><span data-stu-id="acc5c-122">Content-Transfer-Encoding: base64 \*</span></span> 
    
<span data-ttu-id="acc5c-123">En los mensajes salientes, el tipo de contenido debe derivarse de la extensión de tres letras del nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="acc5c-123">On outbound messages, the content-type should be derived from the filename's three-letter extension.</span></span> <span data-ttu-id="acc5c-124">Esta asignación existe en el Registro del sistema; debajo hay un valor de cadena denominado "Tipo de contenido" que proporciona el tipo de contenido MIME si se define uno.</span><span class="sxs-lookup"><span data-stu-id="acc5c-124">This mapping exists in the system registry; under there is a string value named "Content Type" that gives the MIME content type if one is defined.</span></span> <span data-ttu-id="acc5c-125">Este ejemplo es para un archivo de imagen TIFF:</span><span class="sxs-lookup"><span data-stu-id="acc5c-125">This example is for a TIFF image file:</span></span>
  
<span data-ttu-id="acc5c-126">HKEY_LOCAL_MACHINE</span><span class="sxs-lookup"><span data-stu-id="acc5c-126">HKEY_LOCAL_MACHINE</span></span>\
  
<span data-ttu-id="acc5c-127">Software</span><span class="sxs-lookup"><span data-stu-id="acc5c-127">Software</span></span>\
  
<span data-ttu-id="acc5c-128">Microsoft</span><span class="sxs-lookup"><span data-stu-id="acc5c-128">Microsoft</span></span>\
  
<span data-ttu-id="acc5c-129">Clases</span><span class="sxs-lookup"><span data-stu-id="acc5c-129">Classes</span></span>\
  
<span data-ttu-id="acc5c-130">.tif</span><span class="sxs-lookup"><span data-stu-id="acc5c-130">.tif</span></span>
  
<span data-ttu-id="acc5c-131">Tipo de contenido = "image/tiff"</span><span class="sxs-lookup"><span data-stu-id="acc5c-131">Content Type = "image/tiff"</span></span>
  
<span data-ttu-id="acc5c-132">Si no hay ninguna asignación para la extensión de archivo, se debe usar la secuencia predeterminada de la *aplicación/octeto.*</span><span class="sxs-lookup"><span data-stu-id="acc5c-132">If there is no mapping for the file extension, the default  *application/octet*  stream should be used.</span></span> 
  
<span data-ttu-id="acc5c-133">En los mensajes entrantes, el tipo de contenido de un archivo adjunto siempre debe copiarse en la propiedad MAPI PR_ATTACH_MIME_TAG **(** [PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="acc5c-133">On inbound messages, the content-type for an attachment should always be copied to the MAPI property **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span></span> <span data-ttu-id="acc5c-134">Incluso si se define un nombre de archivo para un archivo adjunto, la extensión asignada por el tipo de contenido debe usarse en las propiedades **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) y **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="acc5c-134">Even if a filename is defined for an attached file, the extension mapped by the content-type should be used in the **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) and **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="acc5c-135">Rfc  821 deja oficialmente en desuso el parámetro name.</span><span class="sxs-lookup"><span data-stu-id="acc5c-135">The  *name*  parameter is officially deprecated by RFC 821.</span></span> <span data-ttu-id="acc5c-136">A medida que evolucionan los estándares, Microsoft considerará la posibilidad de especificar una asignación alternativa para los nombres de archivo adjuntos.</span><span class="sxs-lookup"><span data-stu-id="acc5c-136">As standards evolve, Microsoft will consider specifying an alternate mapping for attached filenames.</span></span> 
  
<span data-ttu-id="acc5c-137">Los mensajes adjuntos salientes se envían como \* Tipo de contenido: message/rfc822 \* Los mensajes de los mensajes adjuntos se codifican recursivamente, en su lugar adecuado.</span><span class="sxs-lookup"><span data-stu-id="acc5c-137">Outbound attached messages are sent as \* Content-type: message/rfc822 \*  Messages within attached messages are encoded recursively, in their proper place.</span></span> <span data-ttu-id="acc5c-138">Los elementos de contenido de mensajes entrantes  *con tipo de contenido: multiparte o resumen*  también se asignan a mensajes incrustados.</span><span class="sxs-lookup"><span data-stu-id="acc5c-138">Inbound message content parts with  *Content-Type: multipart/digest*  are also mapped to embedded messages.</span></span> 
  
<span data-ttu-id="acc5c-139">Si uuencode con TNEF se usa al codificar el contenido del mensaje, todas las propiedades de datos adjuntos y el contenido se encuentran en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="acc5c-139">If uuencode with TNEF is used while encoding message content, all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="acc5c-140">El TNEF en sí es un único archivo adjunto binario denominado Winmail.dat, codificado como se describe para Uuencode sin TNEF.</span><span class="sxs-lookup"><span data-stu-id="acc5c-140">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for Uuencode without TNEF.</span></span>
  
<span data-ttu-id="acc5c-141">Si uuencode se usa sin TNEF, todos los archivos adjuntos se tratan como binarios y uuencoded, siguiendo el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="acc5c-141">If uuencode is used without TNEF, all attached files are treated as binary and uuencoded, following the message text.</span></span> <span data-ttu-id="acc5c-142">El nombre del archivo está presente en el encabezado uuencode:</span><span class="sxs-lookup"><span data-stu-id="acc5c-142">The file name is present in the uuencode header:</span></span>
  
 <span data-ttu-id="acc5c-143">begin 0755 Winmail.dat</span><span class="sxs-lookup"><span data-stu-id="acc5c-143">begin 0755 Winmail.dat</span></span> 
  
 <span data-ttu-id="acc5c-144">... datos ...</span><span class="sxs-lookup"><span data-stu-id="acc5c-144">... data ...</span></span> 
  
 <span data-ttu-id="acc5c-145">end</span><span class="sxs-lookup"><span data-stu-id="acc5c-145">end</span></span> 
  
<span data-ttu-id="acc5c-146">Los mensajes adjuntos se textizan en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="acc5c-146">Attached messages are textized into the message text.</span></span> <span data-ttu-id="acc5c-147">La jerarquía de los mensajes adjuntos siempre se aplana; es decir, los mensajes dentro de los mensajes adjuntos se sacan al nivel superior.</span><span class="sxs-lookup"><span data-stu-id="acc5c-147">The hierarchy of attached messages is always flattened; that is, messages within attached messages are pulled out to the top level.</span></span>
  
<span data-ttu-id="acc5c-148">Los objetos OLE incrustados se descartan.</span><span class="sxs-lookup"><span data-stu-id="acc5c-148">Embedded OLE objects are discarded.</span></span>
  
<span data-ttu-id="acc5c-149">Las posiciones de representación de datos adjuntos se transmiten literalmente, mediante la propiedad **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) en el TNEF.</span><span class="sxs-lookup"><span data-stu-id="acc5c-149">Attachment rendering positions are transmitted literally, using the property **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in the TNEF.</span></span> <span data-ttu-id="acc5c-150">Si no se usa TNEF, se pierden.</span><span class="sxs-lookup"><span data-stu-id="acc5c-150">If TNEF is not used, they are lost.</span></span> <span data-ttu-id="acc5c-151">Los datos adjuntos entrantes sin posición de representación (incluso cuando no hay TNEF) tienen su posición de representación establecida en 0xFFFFFFFF, es decir, ninguna posición en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="acc5c-151">Incoming attachments with no rendering position (including when there is no TNEF) have their rendering position set to 0xFFFFFFFF, that is, no position in the message text.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="acc5c-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="acc5c-152">See also</span></span>



[<span data-ttu-id="acc5c-153">Asignación de atributos de correo de Internet a propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="acc5c-153">Mapping of Internet Mail Attributes to MAPI Properties</span></span>](mapping-of-internet-mail-attributes-to-mapi-properties.md)

