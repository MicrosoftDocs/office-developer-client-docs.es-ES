---
title: Analizar el historial de descarga de mensajes de una cuenta POP3
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 394e1430-04d6-4d61-be13-eb695309fa73
description: En este tema se describe la estructura del objeto binario de POP3 que representa el historial de descarga de mensajes de una cuenta POP3, para identificar los mensajes que se han descargado o eliminado en esa cuenta.
ms.openlocfilehash: 44a799f6b6fbe2a2841522c18405149a470b0236
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389011"
---
# <a name="parsing-the-message-download-history-for-a-pop3-account"></a>Analizar el historial de descarga de mensajes de una cuenta POP3

En este tema se describe la estructura del objeto binario de POP3 que representa el historial de descarga de mensajes de una cuenta POP3, para identificar los mensajes que se han descargado o eliminado en esa cuenta.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a>

## <a name="why-parse-the-message-download-history"></a>¿Por qué analizar el historial de descarga de mensajes?

El proveedor de protocolo de oficina de correos (POP) para Outlook permite a los usuarios para recuperar y descargar nuevos mensajes de correo electrónico en su dispositivo local y posteriormente dejar o eliminar estos mensajes de correo electrónico en el servidor de correo. Cuando el cliente de correo comprobaciones para que nuevos mensajes descargar, debe ser capaz de identificar y descargue sólo los mensajes nuevos para esa bandeja de entrada. Para ello, el cliente de correo usando primero el comando UIDL (identificador único anuncio) para obtener un mapa de cada mensaje que nunca se ha entregado a esa bandeja de entrada a un identificador único (UID). El cliente también obtiene el historial de descarga de mensajes para los mensajes que se han descargado o eliminado de la Bandeja de entrada en la que el cliente. Con el mapa UID de mensaje y el historial de descarga, el cliente, a continuación, puede identificar los mensajes que no están presentes en el historial de como nuevo y, por tanto, que debe descargarse.
  
Para obtener el historial de descarga de los mensajes para una bandeja de entrada:
  
- Siga los pasos de [historial para una cuenta POP3 de descarga de encontrar el mensaje](locating-the-message-download-history-for-a-pop3-account.md) para buscar la propiedad [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) , que contiene un objeto binario grande (BLOB) que representa el historial de mensajes de una cuenta POP3. 
    
- Lea este tema, que describe la estructura del objeto binario y se muestra un ejemplo de blobs para identificar los mensajes que se han descargado o eliminado de la Bandeja de entrada de la cuenta POP3.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a>

## <a name="pop-blob-structure"></a>Estructura de BLOB de POP

La estructura de BLOB de POP, tal como se describe en la tabla 1, comienza con dos campos, **versión** y **Count**, seguido de un número de **recuento** de etiquetas de recursos, cada uno de los cuales está terminada en null. 
  
**La tabla 1. Estructura del BLOB que representa el mensaje de historial de descarga de una cuenta POP3**

|**Campo de BLOB**|**Size**|**Descripción**|
|:-----|:-----|:-----|
|**Version** <br/> |2 bytes  <br/> |Debe ser 3 (**PBLOB_VERSION_NUM**).  <br/> |
|**Count** <br/> |2 bytes  <br/> |El número de etiquetas de recurso en este BLOB.  <br/> |
|Etiqueta de recurso  <br/> |Variable  <br/> |cadenas de UTF-8 de 0 o más terminada en null que codifican las etiquetas de recursos. El número de cadenas terminada en null debe coincidir con **recuento**.  <br/> |
   
Cada etiqueta de recurso especifica la operación que se aplica a un mensaje, algunos metadatos de fecha y hora acerca de la operación y codifica el UID del mensaje. El formato de una cadena de la etiqueta de recurso desglosado como se indica a continuación y se explica con más detalle en la tabla 2. 
  
`Ocyyyymmddhhmmssuuu...`
  
**Tabla 2. Estructura de una etiqueta de recurso**

|**Campo en una etiqueta de recurso**|**Size**|**Descripción**|
|:-----|:-----|:-----|
| `O` <br/> |1 carácter  <br/> |La operación se realiza en el mensaje de correo electrónico. El valor debe ser "+", "-", o "&amp;", lo que indica un get correcta, eliminar u operación get y delete, respectivamente.  <br/> |
| `c` <br/> |1 carácter  <br/> |La parte del contenido del mensaje implica en la operación. El valor debe ser "", "h" o "b", que indica el contenido de ninguno, encabezado o cuerpo, respectivamente.  <br/> |
| `yyyy` <br/> |4 caracteres  <br/> |El año de cuatro dígitos de la operación.  <br/> |
| `MM` <br/> |2 caracteres  <br/> |El mes de dos dígitos de la operación.  <br/> |
| `dd` <br/> |2 caracteres  <br/> |El día de dos dígitos de la operación.  <br/> |
| `hh` <br/> |2 caracteres  <br/> |La hora de dos dígitos de la operación.  <br/> |
| `mm` <br/> |2 caracteres  <br/> |Minuto de dos dígitos de la operación.  <br/> |
| `ss` <br/> |2 caracteres  <br/> |El segundo de dos dígitos de la operación.  <br/> |
| `uuu…` <br/> |Longitud variable  <br/> |El UID codificado de un mensaje.  <br/> |

<a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a>

## <a name="example"></a>Ejemplo

En la figura 1 muestra un ejemplo de un objeto binario que representa el historial de descarga de mensajes de una cuenta POP. 
  
**En la figura 1. Ejemplo de estructura de blobs para el mensaje de historial de descarga de una cuenta POP3**

![BLOB del historial de descarga de mensajes de cuenta POP3](media/OL15Con_AuxRef_ParsingMsgsHistory_Blob.gif)
  
En función de la estructura que se describen en la tabla 1 y 2 de la tabla, este BLOB representa el historial de descarga de mensajes de correo electrónico 23.
  
Para analizar el UID sin procesar en cada etiqueta de recursos, tenga en cuenta que el UID sigue esta codificación: caracteres en un UID son principalmente caracteres alfanuméricos, y cada carácter no alfanumérico está precedido por el carácter ASCII "$" (0 x 24). Por lo que los caracteres ASCII $2d representan el no alfanuméricos carácter "-". La figura 2 muestra un ejemplo de convertir en primer lugar el UID sin procesar en la etiqueta de recurso 1 a la representación ASCII, a continuación, convertir cualquier carácter no alfanumérico precedido por "$" para producir el UID real:
  
`0BC535DB-EA63-11E1-A75C-00215AD7BB74`
  
**La figura 2. Convertir el UID sin procesar en una etiqueta de recurso para el mensaje real de UID**

![Conversión de UID sin procesar en BLOB a UID de mensaje real](media/OL15Con_AuxRef_ParsingMsgsHistory_BlobRscTag.gif)
  
Para interpretar la etiqueta de recurso 1 en este BLOB: el mensaje con el identificador exclusivo `0BC535DB-EA63-11E1-A75C-00215AD7BB74` se recuperó correctamente en 6 de septiembre de 2012, en 13:11:38. 
  
De forma similar puede analizar las etiquetas restantes de 22 recurso de BLOB.
  
## <a name="see-also"></a>Vea también
<a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a>

- [Administrar la descarga de mensajes de las cuentas POP3](managing-message-downloads-for-pop3-accounts.md)    
- [Localizar el historial de descarga de mensajes de una cuenta POP3](locating-the-message-download-history-for-a-pop3-account.md)    
- [Analizar el historial UIDL de POP3](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/04/parsing-the-pop3-uidl-history.aspx)
    

