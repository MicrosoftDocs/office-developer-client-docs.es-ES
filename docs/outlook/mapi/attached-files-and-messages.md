---
title: Mensajes y archivos adjuntos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b2f2fb72-23ae-4e0b-a8a1-3b78a1862acb
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d5b37ea2e254e05ada3214309f58147e92f46393
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566834"
---
# <a name="attached-files-and-messages"></a><span data-ttu-id="49068-103">Mensajes y archivos adjuntos</span><span class="sxs-lookup"><span data-stu-id="49068-103">Attached Files and Messages</span></span>

  
  
<span data-ttu-id="49068-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49068-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49068-105">Si MIME con TNEF se usa durante la codificación de contenido del mensaje, todo el contenido y las propiedades de los datos adjuntos se encuentran en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="49068-105">If MIME with TNEF is used while encoding message content,all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="49068-106">La codificación TNEF propio es un único archivo adjunto binario denominado Winmail.dat, con codificación tal como se describe para MIME sin TNEF.</span><span class="sxs-lookup"><span data-stu-id="49068-106">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for MIME without TNEF.</span></span> 
  
<span data-ttu-id="49068-107">Si se usa MIME sin TNEF, los archivos adjuntos se envían como elementos de contenido de mensaje MIME.</span><span class="sxs-lookup"><span data-stu-id="49068-107">If MIME is used without TNEF, attached files are sent as MIME message content parts.</span></span> <span data-ttu-id="49068-108">El nombre de archivo se coloca en el parámetro *name* al encabezado *Content-type* para los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="49068-108">The filename is placed in the  *name*  parameter to the  *Content-type*  header for the attachment.</span></span> <span data-ttu-id="49068-109">El juego de caracteres para los datos adjuntos se colocan en el parámetro *charset* en el *Content-type* ; junto con el contenido de codificación de transferencia se determinan mediante el examen el contenido de datos adjuntos completo.</span><span class="sxs-lookup"><span data-stu-id="49068-109">The character set for the attachment is placed in the  *charset*  parameter to the  *Content-type*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content.</span></span> <span data-ttu-id="49068-110">Datos adjuntos de la dirección URL se tratan especialmente:</span><span class="sxs-lookup"><span data-stu-id="49068-110">URL attachments are treated specially:</span></span> 
  
- <span data-ttu-id="49068-111">Si los datos adjuntos están una dirección URL (es decir, un archivo adjunto con la extensión. Dirección URL) y el modo de acceso definido en ella es FTP anónimo, éste se codifica como un mensaje externo y se copia el contenido del archivo (la dirección URL) en el encabezado del mensaje externo.</span><span class="sxs-lookup"><span data-stu-id="49068-111">If the attachment is a URL (an attached file with extension .URL), and the access mode defined in it is anonymous FTP, it is encoded as an external message, and the content of the file (the URL) is copied into the header of the external message.</span></span> <span data-ttu-id="49068-112">*Content-type: cuerpo del mensaje o externo; el tipo de acceso = anon ftp*  (Codificación de transferencia de contenido: se supone de 7 bits.)</span><span class="sxs-lookup"><span data-stu-id="49068-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span></span> 
    
- <span data-ttu-id="49068-113">Si sólo se encuentran caracteres de 7 bits y línea no supera 140 caracteres de longitud, los datos adjuntos son texto ASCII.</span><span class="sxs-lookup"><span data-stu-id="49068-113">If only 7-bit characters are found and no line exceeds 140 characters in length, the attachment is ASCII text.</span></span> <span data-ttu-id="49068-114">*Tipo de contenido: texto sin formato; charset = us-ascii Content-Transfer-Encoding: 7 bits*</span><span class="sxs-lookup"><span data-stu-id="49068-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span></span> 
    
- <span data-ttu-id="49068-115">Si las líneas de largo o copia de seguridad en un 25% 8 bits se encuentran caracteres, el contenido de los datos adjuntos es un texto y el juego de caracteres está determinado por la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="49068-115">If long lines or up to 25% 8-bit characters are found, the attachment content is text and the character set is determined by the locale.</span></span> <span data-ttu-id="49068-116">Se debe proceder de los conjuntos de caracteres definidos por ISO 8859 estándar.</span><span class="sxs-lookup"><span data-stu-id="49068-116">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="49068-117">*Content-type: texto sin formato; charset = ISO-8859-1*  (por ejemplo)</span><span class="sxs-lookup"><span data-stu-id="49068-117">*Content-type: text/plain; charset=ISO-8859-1*  (for example)</span></span> 
    
     <span data-ttu-id="49068-118">*Content-Transfer-Encoding: quoted-printable*</span><span class="sxs-lookup"><span data-stu-id="49068-118">*Content-Transfer-Encoding: quoted-printable*</span></span> 
    
- <span data-ttu-id="49068-119">Si el 25% o más de los caracteres tienen el bit alto establecido, los datos adjuntos son binario.</span><span class="sxs-lookup"><span data-stu-id="49068-119">If 25% or more of the characters have the high bit set, the attachment is binary.</span></span> <span data-ttu-id="49068-120">Se codifica mediante el algoritmo Base64.</span><span class="sxs-lookup"><span data-stu-id="49068-120">It is encoded using the Base64 algorithm.</span></span> <span data-ttu-id="49068-121">*Content-type: aplicación/flujo de octetos*  (de forma predeterminada; en función de extensión de archivo)</span><span class="sxs-lookup"><span data-stu-id="49068-121">*Content-type: application/octet-stream*  (by default; based on file extension)</span></span> 
    
     * <span data-ttu-id="49068-122">Content-Transfer-Encoding: base64 \*</span><span class="sxs-lookup"><span data-stu-id="49068-122">Content-Transfer-Encoding: base64 \*</span></span> 
    
<span data-ttu-id="49068-123">En los mensajes salientes, el tipo de contenido se debe derivar de extensión de tres letras del nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="49068-123">On outbound messages, the content-type should be derived from the filename's three-letter extension.</span></span> <span data-ttu-id="49068-124">Esta asignación existe en el registro del sistema; bajo allí es un valor de cadena denominado "Tipo de contenido" que proporciona el tipo de contenido MIME si se define uno.</span><span class="sxs-lookup"><span data-stu-id="49068-124">This mapping exists in the system registry; under there is a string value named "Content Type" that gives the MIME content type if one is defined.</span></span> <span data-ttu-id="49068-125">Este ejemplo es para un archivo de imagen TIFF:</span><span class="sxs-lookup"><span data-stu-id="49068-125">This example is for a TIFF image file:</span></span>
  
<span data-ttu-id="49068-126">HKEY_LOCAL_MACHINE\\</span><span class="sxs-lookup"><span data-stu-id="49068-126">HKEY_LOCAL_MACHINE\\</span></span>
  
<span data-ttu-id="49068-127">Software\\</span><span class="sxs-lookup"><span data-stu-id="49068-127">Software\\</span></span>
  
<span data-ttu-id="49068-128">Microsoft\\</span><span class="sxs-lookup"><span data-stu-id="49068-128">Microsoft\\</span></span>
  
<span data-ttu-id="49068-129">Classes\\</span><span class="sxs-lookup"><span data-stu-id="49068-129">Classes\\</span></span>
  
<span data-ttu-id="49068-130">.TIF</span><span class="sxs-lookup"><span data-stu-id="49068-130">.tif</span></span>
  
<span data-ttu-id="49068-131">Tipo de contenido = "imagen: tiff"</span><span class="sxs-lookup"><span data-stu-id="49068-131">Content Type = "image/tiff"</span></span>
  
<span data-ttu-id="49068-132">Si no hay ninguna asignación para la extensión de archivo, se debe usar la secuencia de *octetos/aplicación* predeterminada.</span><span class="sxs-lookup"><span data-stu-id="49068-132">If there is no mapping for the file extension, the default  *application/octet*  stream should be used.</span></span> 
  
<span data-ttu-id="49068-133">En los mensajes entrantes, el tipo de contenido para los datos adjuntos siempre debe copiarse a la propiedad MAPI **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="49068-133">On inbound messages, the content-type for an attachment should always be copied to the MAPI property **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span></span> <span data-ttu-id="49068-134">Incluso si se define un nombre de archivo para un archivo adjunto, debe usarse la extensión asignada por el tipo de contenido en las propiedades de **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) y **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="49068-134">Even if a filename is defined for an attached file, the extension mapped by the content-type should be used in the **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) and **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="49068-135">El parámetro *name* oficialmente está en desuso por RFC 821.</span><span class="sxs-lookup"><span data-stu-id="49068-135">The  *name*  parameter is officially deprecated by RFC 821.</span></span> <span data-ttu-id="49068-136">Como estándares evolucionen, Microsoft se considere la posibilidad de especificar una asignación alternativa para nombres de archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="49068-136">As standards evolve, Microsoft will consider specifying an alternate mapping for attached filenames.</span></span> 
  
<span data-ttu-id="49068-137">Se envían los mensajes salientes de adjuntos como * Content-type: mensaje/rfc822 * mensajes dentro de mensajes adjuntos son codificado de forma recursiva, en su lugar correcto.</span><span class="sxs-lookup"><span data-stu-id="49068-137">Outbound attached messages are sent as * Content-type: message/rfc822 *  Messages within attached messages are encoded recursively, in their proper place.</span></span> <span data-ttu-id="49068-138">Entrada de elementos de contenido de mensaje con *Content-Type: multipart/implícita* también se asignan a los mensajes incrustados.</span><span class="sxs-lookup"><span data-stu-id="49068-138">Inbound message content parts with  *Content-Type: multipart/digest*  are also mapped to embedded messages.</span></span> 
  
<span data-ttu-id="49068-139">Si uuencode con TNEF se usa durante la codificación de contenido del mensaje, todo el contenido y las propiedades de los datos adjuntos se encuentran en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="49068-139">If uuencode with TNEF is used while encoding message content, all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="49068-140">La codificación TNEF propio es un único archivo adjunto binario denominado Winmail.dat, con codificación tal como se describe para Uuencode sin TNEF.</span><span class="sxs-lookup"><span data-stu-id="49068-140">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for Uuencode without TNEF.</span></span>
  
<span data-ttu-id="49068-141">Si se usa uuencode sin TNEF, todos los archivos adjuntos se tratan como binarios y formato uuencode, siguiendo el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="49068-141">If uuencode is used without TNEF, all attached files are treated as binary and uuencoded, following the message text.</span></span> <span data-ttu-id="49068-142">El nombre de archivo está presente en el encabezado uuencode:</span><span class="sxs-lookup"><span data-stu-id="49068-142">The file name is present in the uuencode header:</span></span>
  
 <span data-ttu-id="49068-143">comenzar 0755 Winmail.dat</span><span class="sxs-lookup"><span data-stu-id="49068-143">begin 0755 Winmail.dat</span></span> 
  
 <span data-ttu-id="49068-144">… datos...</span><span class="sxs-lookup"><span data-stu-id="49068-144">... data ...</span></span> 
  
 <span data-ttu-id="49068-145">end</span><span class="sxs-lookup"><span data-stu-id="49068-145">end</span></span> 
  
<span data-ttu-id="49068-146">Mensajes adjuntos son convertir a texto en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="49068-146">Attached messages are textized into the message text.</span></span> <span data-ttu-id="49068-147">La jerarquía de mensajes adjuntos siempre se acopla; es decir, los mensajes dentro de mensajes adjuntos se extraen al nivel superior.</span><span class="sxs-lookup"><span data-stu-id="49068-147">The hierarchy of attached messages is always flattened; that is, messages within attached messages are pulled out to the top level.</span></span>
  
<span data-ttu-id="49068-148">Objetos OLE incrustados se descartan.</span><span class="sxs-lookup"><span data-stu-id="49068-148">Embedded OLE objects are discarded.</span></span>
  
<span data-ttu-id="49068-149">Posiciones de procesamiento de datos adjuntos se transmiten literalmente, mediante la propiedad **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) en la codificación TNEF.</span><span class="sxs-lookup"><span data-stu-id="49068-149">Attachment rendering positions are transmitted literally, using the property **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in the TNEF.</span></span> <span data-ttu-id="49068-150">Si no se usa la codificación TNEF, se pierden.</span><span class="sxs-lookup"><span data-stu-id="49068-150">If TNEF is not used, they are lost.</span></span> <span data-ttu-id="49068-151">Datos adjuntos entrantes con ninguna posición de representación (incluso cuando no hay ningún TNEF) tienen su posición de representación no establecida en 0xFFFFFFFF, es decir, ninguna posición en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="49068-151">Incoming attachments with no rendering position (including when there is no TNEF) have their rendering position set to 0xFFFFFFFF, that is, no position in the message text.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="49068-152">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="49068-152">See also</span></span>



[<span data-ttu-id="49068-153">Asignación de atributos de correo de Internet a las propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="49068-153">Mapping of Internet Mail Attributes to MAPI Properties</span></span>](mapping-of-internet-mail-attributes-to-mapi-properties.md)

