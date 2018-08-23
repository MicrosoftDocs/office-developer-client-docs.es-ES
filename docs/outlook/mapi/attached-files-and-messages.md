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
# <a name="attached-files-and-messages"></a>Mensajes y archivos adjuntos

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Si MIME con TNEF se usa durante la codificación de contenido del mensaje, todo el contenido y las propiedades de los datos adjuntos se encuentran en la secuencia TNEF. La codificación TNEF propio es un único archivo adjunto binario denominado Winmail.dat, con codificación tal como se describe para MIME sin TNEF. 
  
Si se usa MIME sin TNEF, los archivos adjuntos se envían como elementos de contenido de mensaje MIME. El nombre de archivo se coloca en el parámetro *name* al encabezado *Content-type* para los datos adjuntos. El juego de caracteres para los datos adjuntos se colocan en el parámetro *charset* en el *Content-type* ; junto con el contenido de codificación de transferencia se determinan mediante el examen el contenido de datos adjuntos completo. Datos adjuntos de la dirección URL se tratan especialmente: 
  
- Si los datos adjuntos están una dirección URL (es decir, un archivo adjunto con la extensión. Dirección URL) y el modo de acceso definido en ella es FTP anónimo, éste se codifica como un mensaje externo y se copia el contenido del archivo (la dirección URL) en el encabezado del mensaje externo. *Content-type: cuerpo del mensaje o externo; el tipo de acceso = anon ftp*  (Codificación de transferencia de contenido: se supone de 7 bits.) 
    
- Si sólo se encuentran caracteres de 7 bits y línea no supera 140 caracteres de longitud, los datos adjuntos son texto ASCII. *Tipo de contenido: texto sin formato; charset = us-ascii Content-Transfer-Encoding: 7 bits* 
    
- Si las líneas de largo o copia de seguridad en un 25% 8 bits se encuentran caracteres, el contenido de los datos adjuntos es un texto y el juego de caracteres está determinado por la configuración regional. Se debe proceder de los conjuntos de caracteres definidos por ISO 8859 estándar. *Content-type: texto sin formato; charset = ISO-8859-1*  (por ejemplo) 
    
     *Content-Transfer-Encoding: quoted-printable* 
    
- Si el 25% o más de los caracteres tienen el bit alto establecido, los datos adjuntos son binario. Se codifica mediante el algoritmo Base64. *Content-type: aplicación/flujo de octetos*  (de forma predeterminada; en función de extensión de archivo) 
    
     * Content-Transfer-Encoding: base64 * 
    
En los mensajes salientes, el tipo de contenido se debe derivar de extensión de tres letras del nombre de archivo. Esta asignación existe en el registro del sistema; bajo allí es un valor de cadena denominado "Tipo de contenido" que proporciona el tipo de contenido MIME si se define uno. Este ejemplo es para un archivo de imagen TIFF:
  
HKEY_LOCAL_MACHINE\
  
Software\
  
Microsoft\
  
Classes\
  
.TIF
  
Tipo de contenido = "imagen: tiff"
  
Si no hay ninguna asignación para la extensión de archivo, se debe usar la secuencia de *octetos/aplicación* predeterminada. 
  
En los mensajes entrantes, el tipo de contenido para los datos adjuntos siempre debe copiarse a la propiedad MAPI **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)). Incluso si se define un nombre de archivo para un archivo adjunto, debe usarse la extensión asignada por el tipo de contenido en las propiedades de **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) y **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) .
  
El parámetro *name* oficialmente está en desuso por RFC 821. Como estándares evolucionen, Microsoft se considere la posibilidad de especificar una asignación alternativa para nombres de archivo adjunto. 
  
Se envían los mensajes salientes de adjuntos como * Content-type: mensaje/rfc822 * mensajes dentro de mensajes adjuntos son codificado de forma recursiva, en su lugar correcto. Entrada de elementos de contenido de mensaje con *Content-Type: multipart/implícita* también se asignan a los mensajes incrustados. 
  
Si uuencode con TNEF se usa durante la codificación de contenido del mensaje, todo el contenido y las propiedades de los datos adjuntos se encuentran en la secuencia TNEF. La codificación TNEF propio es un único archivo adjunto binario denominado Winmail.dat, con codificación tal como se describe para Uuencode sin TNEF.
  
Si se usa uuencode sin TNEF, todos los archivos adjuntos se tratan como binarios y formato uuencode, siguiendo el texto del mensaje. El nombre de archivo está presente en el encabezado uuencode:
  
 comenzar 0755 Winmail.dat 
  
 … datos... 
  
 end 
  
Mensajes adjuntos son convertir a texto en el texto del mensaje. La jerarquía de mensajes adjuntos siempre se acopla; es decir, los mensajes dentro de mensajes adjuntos se extraen al nivel superior.
  
Objetos OLE incrustados se descartan.
  
Posiciones de procesamiento de datos adjuntos se transmiten literalmente, mediante la propiedad **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) en la codificación TNEF. Si no se usa la codificación TNEF, se pierden. Datos adjuntos entrantes con ninguna posición de representación (incluso cuando no hay ningún TNEF) tienen su posición de representación no establecida en 0xFFFFFFFF, es decir, ninguna posición en el texto del mensaje.
  
## <a name="see-also"></a>Recursos adicionales



[Asignación de atributos de correo de Internet a las propiedades MAPI](mapping-of-internet-mail-attributes-to-mapi-properties.md)

