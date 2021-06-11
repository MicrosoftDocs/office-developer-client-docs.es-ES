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
# <a name="attached-files-and-messages"></a>Archivos y mensajes adjuntos

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Si se usa MIME con TNEF al codificar el contenido del mensaje, todas las propiedades de datos adjuntos y el contenido se encuentran en la secuencia TNEF. El TNEF en sí es un único archivo adjunto binario denominado Winmail.dat, codificado como se describe para MIME sin TNEF. 
  
Si se usa MIME sin TNEF, los archivos adjuntos se envían como elementos de contenido de mensajes MIME. El nombre de archivo se coloca en el  *parámetro name*  en el  *encabezado Content-type*  para los datos adjuntos. El juego de caracteres para los datos adjuntos se coloca en el  *parámetro charset*  al  *tipo Content*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content. Los datos adjuntos de dirección URL se tratan especialmente: 
  
- Si los datos adjuntos son una dirección URL (un archivo adjunto con extensión . URL), y el modo de acceso definido en él es FTP anónimo, se codifica como un mensaje externo y el contenido del archivo (la dirección URL) se copia en el encabezado del mensaje externo. *Tipo de contenido: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bits se supone). 
    
- Si solo se encuentran caracteres de 7 bits y ninguna línea supera los 140 caracteres de longitud, los datos adjuntos son texto ASCII. *Tipo de contenido: texto/sin formato; charset=us-ascii Content-Transfer-Encoding: 7bits* 
    
- Si se encuentran líneas largas o hasta un 25 % de caracteres de 8 bits, el contenido de los datos adjuntos es texto y el juego de caracteres lo determina la configuración regional. Debe elegirse entre los conjuntos de caracteres definidos por la norma ISO 8859. *Tipo de contenido: texto/sin formato; charset=ISO-8859-1*  (por ejemplo) 
    
     *Content-Transfer-Encoding: quoted-printable* 
    
- Si el 25 % o más de los caracteres tienen el conjunto de bits alto, los datos adjuntos son binarios. Se codifica mediante el algoritmo Base64. *Tipo de contenido: application/octet-stream*  (de forma predeterminada, en función de la extensión de archivo) 
    
     * Content-Transfer-Encoding: base64 * 
    
En los mensajes salientes, el tipo de contenido debe derivarse de la extensión de tres letras del nombre de archivo. Esta asignación existe en el Registro del sistema; debajo hay un valor de cadena denominado "Tipo de contenido" que proporciona el tipo de contenido MIME si se define uno. Este ejemplo es para un archivo de imagen TIFF:
  
HKEY_LOCAL_MACHINE\
  
Software\
  
Microsoft\
  
Clases\
  
.tif
  
Tipo de contenido = "image/tiff"
  
Si no hay ninguna asignación para la extensión de archivo, se debe usar la secuencia predeterminada de la *aplicación/octeto.* 
  
En los mensajes entrantes, el tipo de contenido de un archivo adjunto siempre debe copiarse en la propiedad MAPI PR_ATTACH_MIME_TAG **(** [PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)). Incluso si se define un nombre de archivo para un archivo adjunto, la extensión asignada por el tipo de contenido debe usarse en las propiedades **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) y **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)).
  
Rfc  821 deja oficialmente en desuso el parámetro name. A medida que evolucionan los estándares, Microsoft considerará la posibilidad de especificar una asignación alternativa para los nombres de archivo adjuntos. 
  
Los mensajes adjuntos salientes se envían como * Tipo de contenido: message/rfc822 * Los mensajes de los mensajes adjuntos se codifican recursivamente, en su lugar adecuado. Los elementos de contenido de mensajes entrantes  *con tipo de contenido: multiparte o resumen*  también se asignan a mensajes incrustados. 
  
Si uuencode con TNEF se usa al codificar el contenido del mensaje, todas las propiedades de datos adjuntos y el contenido se encuentran en la secuencia TNEF. El TNEF en sí es un único archivo adjunto binario denominado Winmail.dat, codificado como se describe para Uuencode sin TNEF.
  
Si uuencode se usa sin TNEF, todos los archivos adjuntos se tratan como binarios y uuencoded, siguiendo el texto del mensaje. El nombre del archivo está presente en el encabezado uuencode:
  
 begin 0755 Winmail.dat 
  
 ... datos ... 
  
 end 
  
Los mensajes adjuntos se textizan en el texto del mensaje. La jerarquía de los mensajes adjuntos siempre se aplana; es decir, los mensajes dentro de los mensajes adjuntos se sacan al nivel superior.
  
Los objetos OLE incrustados se descartan.
  
Las posiciones de representación de datos adjuntos se transmiten literalmente, mediante la propiedad **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) en el TNEF. Si no se usa TNEF, se pierden. Los datos adjuntos entrantes sin posición de representación (incluso cuando no hay TNEF) tienen su posición de representación establecida en 0xFFFFFFFF, es decir, ninguna posición en el texto del mensaje.
  
## <a name="see-also"></a>Vea también



[Asignación de atributos de correo de Internet a propiedades MAPI](mapping-of-internet-mail-attributes-to-mapi-properties.md)

