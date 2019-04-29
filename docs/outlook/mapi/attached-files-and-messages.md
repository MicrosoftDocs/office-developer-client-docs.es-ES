---
title: Archivos adJuntos y mensajes
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
# <a name="attached-files-and-messages"></a>Archivos adJuntos y mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Si se usa MIME con TNEF al codificar el contenido de los mensajes, todas las propiedades y el contenido de los datos adjuntos se encuentran en la secuencia TNEF. El propio TNEF es un único archivo adjunto binario denominado Winmail. dat, codificado como se describe para MIME sin TNEF. 
  
Si se usa MIME sin TNEF, los archivos adjuntos se envían como elementos de contenido de mensajes MIME. El nombre de archivo se coloca en el parámetro *Name* en el encabezado *Content-Type* para los datos adjuntos. El juego de caracteres para los datos adjuntos se coloca en el parámetro *CharSet* para *Content-Type* ; y la codificación de transferencia de contenido se determinan examinando todo el contenido de los datos adjuntos. Los datos adjuntos de dirección URL se tratan de manera especial: 
  
- Si los datos adjuntos son una dirección URL (un archivo adjunto con la extensión. URL) y el modo de acceso definido en él es FTP anónimo, se codifica como un mensaje externo y el contenido del archivo (la dirección URL) se copia en el encabezado del mensaje externo. *Tipo de contenido: mensaje/externo-cuerpo; tipo de acceso = Anon-FTP*  (Se supone que se trata de la codificación de transferencia de contenido: 7). 
    
- Si solo se encuentran caracteres de 7 bits y ninguna línea supera los 140 caracteres de longitud, los datos adjuntos son de texto ASCII. *Tipo de contenido: texto/sin formato; charset = US-ASCII Content-Transfer-Encoding: 7* 
    
- Si se encuentran líneas largas o caracteres de un 25% de 8 bits, el contenido de los datos adjuntos es texto y el juego de caracteres lo determina la configuración regional. Debe elegirse a partir de los juegos de caracteres definidos por la norma ISO 8859. *Content-Type: text/plain; charset = ISO-8859-1*  (por ejemplo) 
    
     *Content-Transfer-Encoding: quoted-printable* 
    
- Si el 25% o más de los caracteres tienen el bit alto establecido, los datos adjuntos son binarios. Se codifica mediante el algoritmo Base64. *Content-Type: application/octet-stream*  (de forma predeterminada, según la extensión de archivo) 
    
     * Codificación de transferencia de contenido: Base64 * 
    
En los mensajes salientes, el tipo de contenido debe derivarse de la extensión de tres letras del nombre de archivo. Esta asignación existe en el registro del sistema; bajo hay un valor de cadena denominado "Content Type" que proporciona el tipo de contenido MIME si se define uno. Este es un ejemplo de un archivo de imagen TIFF:
  
HKEY_LOCAL_MACHINE \
  
Aplicaciones
  
Microsoft
  
Clases
  
. tif
  
Tipo de contenido = "imagen/TIFF"
  
Si no hay ninguna asignación para la extensión de archivo, debe usarse la secuencia de *octetos/aplicación* predeterminada. 
  
En los mensajes entrantes, el tipo de contenido de los datos adjuntos siempre debe copiarse a la propiedad MAPI **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)). Incluso si se define un nombre de archivo para un archivo adjunto, se debe usar la extensión asignada por el tipo de contenido en las propiedades **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) y **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)). .
  
El parámetro *Name* está obsoleto oficialmente en RFC 821. A medida que los estándares evolucionen, Microsoft considerará la especificación de una asignación alternativa para los nombres de archivo adjuntos. 
  
Los mensajes adjuntos salientes se envían como * Content-Type: Message/rfc822 * los mensajes adjuntos de los mensajes adjuntos se codifican de forma recursiva en el mismo espacio. Los elementos de contenido de los mensajes entrantes con *Content-Type: multipart/Digest* también se asignan a los mensajes incrustados. 
  
Si se usa uuencode con TNEF al codificar el contenido de los mensajes, todas las propiedades y el contenido de los datos adjuntos estarán en la secuencia TNEF. El propio TNEF es un único archivo adjunto binario denominado Winmail. dat, codificado como se describe para uuencode sin TNEF.
  
Si se usa uuencode sin TNEF, todos los archivos adjuntos se tratan como binarios y uuencode, siguiendo el texto del mensaje. El nombre de archivo está presente en el encabezado uuencode:
  
 comenzar 0755 Winmail. dat 
  
 ... datos... 
  
 finalización 
  
Los mensajes adJuntos se texto en el texto del mensaje. La jerarquía de los mensajes adjuntos es siempre plana; es decir, los mensajes incluidos en los mensajes adjuntos se extraen al nivel superior.
  
Los objetos OLE incrustados se descartan.
  
Las posiciones de representación de datos adJuntos se transmiten literalmente, mediante la propiedad **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) de la TNEF. Si no se usa TNEF, se pierden. Los datos adjuntos entrantes sin posición de representación (incluso cuando no hay TNEF) tienen su posición de representación establecida en 0xFFFFFFFF, es decir, ninguna posición en el texto del mensaje.
  
## <a name="see-also"></a>Ver también



[Asignación de atributos de correo de Internet a las propiedades MAPI](mapping-of-internet-mail-attributes-to-mapi-properties.md)

