---
title: Analizar el historial de descarga de mensajes de una cuenta POP3
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 394e1430-04d6-4d61-be13-eb695309fa73
description: En este tema se describe la estructura del BLOB DE POP3 que representa el historial de descarga de mensajes de una cuenta POP3, para identificar los mensajes que se han descargado o eliminado en esa cuenta.
ms.openlocfilehash: 44a799f6b6fbe2a2841522c18405149a470b0236
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327772"
---
# <a name="parsing-the-message-download-history-for-a-pop3-account"></a>Analizar el historial de descarga de mensajes de una cuenta POP3

En este tema se describe la estructura del BLOB DE POP3 que representa el historial de descarga de mensajes de una cuenta POP3, para identificar los mensajes que se han descargado o eliminado en esa cuenta.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_WhyParseHistory"> </a>

## <a name="why-parse-the-message-download-history"></a>¿Por qué analizar el historial de descarga de mensajes?

El proveedor de protocolo post Office (POP) para Outlook permite a los usuarios recuperar y descargar nuevos mensajes de correo electrónico en su dispositivo local y, posteriormente, dejar o eliminar estos mensajes de correo electrónico en el servidor de correo. Cuando el cliente de correo comprueba si hay nuevos mensajes que descargar, debe poder identificar y descargar solo los nuevos mensajes de esa Bandeja de entrada. Para ello, el cliente de correo usa primero el comando UIDL (Unique ID Listing) para obtener un mapa de cada mensaje que se haya entregado a esa Bandeja de entrada a un identificador único (UID). El cliente también obtiene el historial de descarga de mensajes para los mensajes que se han descargado o eliminado para la Bandeja de entrada en ese cliente. Con el mapa uid del mensaje y el historial de descarga, el cliente puede identificar los mensajes que no están en el historial como nuevos y, por lo tanto, debe descargarse.
  
Para obtener el historial de descarga de mensajes de una Bandeja de entrada:
  
- Siga los pasos descritos en Localizar el historial de descarga de mensajes de una cuenta [POP3](locating-the-message-download-history-for-a-pop3-account.md) para buscar la propiedad [PidTagAttachDataBinary,](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) que contiene un objeto binario grande (BLOB) que representa el historial de mensajes de una cuenta POP3. 
    
- Lea este tema, que describe la estructura del BLOB y muestra un blob de ejemplo para identificar los mensajes que se han descargado o eliminado para la Bandeja de entrada de la cuenta POP3.

<a name="OL15Con_AuxRef_ParsingMsgsHistory_BLOBStructure"> </a>

## <a name="pop-blob-structure"></a>Estructura DE BLOB POP

La estructura POP BLOB, tal como se describe en la tabla 1, comienza con dos campos, **Version** y **Count**, seguidos de un **número** count de etiquetas de recursos, cada una de las cuales termina en null. 
  
**Tabla 1. Estructura del BLOB que representa el historial de descarga de mensajes de una cuenta POP3**

|**Campo en BLOB**|**Tamaño**|**Descripción**|
|:-----|:-----|:-----|
|**Versión** <br/> |2 bytes  <br/> |Debe ser 3 (**PBLOB_VERSION_NUM**).  <br/> |
|**Count** <br/> |2 bytes  <br/> |Número de etiquetas de recursos en este BLOB.  <br/> |
|Etiqueta de recursos  <br/> |Variable  <br/> |0 o más cadenas UTF-8 terminadas en null que codifican las etiquetas de recursos. El número de cadenas terminadas en null debe coincidir con **Count**.  <br/> |
   
Cada etiqueta de recurso especifica la operación que se aplica a un mensaje, algunos metadatos de fecha y hora sobre la operación y codifica el UID del mensaje. El formato de una cadena de etiqueta de recurso se desglosa de la siguiente manera y se explica más adelante en la tabla 2. 
  
`Ocyyyymmddhhmmssuuu...`
  
**Tabla 2. Estructura de una etiqueta de recurso**

|**Campo en una etiqueta de recurso**|**Tamaño**|**Descripción**|
|:-----|:-----|:-----|
| `O` <br/> |1 carácter  <br/> |Operación realizada en el mensaje de correo electrónico. El valor debe ser "+", "-" o " ", lo que indica una operación &amp; get, delete o get-and-delete correcta, respectivamente.  <br/> |
| `c` <br/> |1 carácter  <br/> |Parte del contenido del mensaje implicado en la operación. El valor debe ser " ", "h" o "b", que indica el contenido de ninguno, encabezado o cuerpo, respectivamente.  <br/> |
| `yyyy` <br/> |4 caracteres  <br/> |Año de cuatro dígitos de la operación.  <br/> |
| `MM` <br/> |2 caracteres  <br/> |El mes de dos dígitos de la operación.  <br/> |
| `dd` <br/> |2 caracteres  <br/> |El día de dos dígitos de la operación.  <br/> |
| `hh` <br/> |2 caracteres  <br/> |Hora de dos dígitos de la operación.  <br/> |
| `mm` <br/> |2 caracteres  <br/> |Minuto de dos dígitos de la operación.  <br/> |
| `ss` <br/> |2 caracteres  <br/> |Segundo de dos dígitos de la operación.  <br/> |
| `uuu…` <br/> |Longitud variable  <br/> |Uid codificado de un mensaje.  <br/> |

<a name="OL15Con_AuxRef_ParsingMsgsHistory_Example"> </a>

## <a name="example"></a>Ejemplo

En la figura 1 se muestra un ejemplo de blob que representa el historial de descarga de mensajes de una cuenta POP. 
  
**Figura 1. Estructura BLOB de ejemplo para el historial de descarga de mensajes de una cuenta POP3**

![BLOB del historial de descarga de mensajes de cuenta POP3](media/OL15Con_AuxRef_ParsingMsgsHistory_Blob.gif)
  
En función de la estructura descrita en las tablas 1 y 2, este BLOB representa el historial de descarga de 23 mensajes de correo electrónico.
  
Para analizar el UID sin procesar en cada etiqueta de recurso, tenga en cuenta que el UID sigue esta codificación: los caracteres de un UID son principalmente caracteres alfanuméricos y cada carácter no alfanumérico está precedido por el carácter ASCII "$" (0x24). Por lo tanto, los caracteres ASCII $2d representan el carácter no alfanumérico "-". En la figura 2 se muestra un ejemplo de convertir primero el UID sin procesar en la etiqueta de recurso 1 a la representación ASCII y, a continuación, convertir cualquier carácter no alfanumérico precedido de "$" para producir el UID real:
  
`0BC535DB-EA63-11E1-A75C-00215AD7BB74`
  
**Figura 2. Convertir el UID sin procesar en una etiqueta de recurso al uid de mensaje real**

![Conversión de UID sin procesar en BLOB a UID de mensaje real](media/OL15Con_AuxRef_ParsingMsgsHistory_BlobRscTag.gif)
  
Para interpretar la etiqueta de recurso 1 en este BLOB: el mensaje con el UID se recuperó correctamente el 6 de septiembre de  `0BC535DB-EA63-11E1-A75C-00215AD7BB74` 2012 a las 13:11:38. 
  
De forma similar, puede analizar las 22 etiquetas de recursos restantes para ese BLOB.
  
## <a name="see-also"></a>Vea también
<a name="OL15Con_AuxRef_ParsingMsgsHistory_AdditionalRsc"> </a>

- [Administrar la descarga de mensajes de las cuentas POP3](managing-message-downloads-for-pop3-accounts.md)    
- [Localizar el historial de descarga de mensajes de una cuenta POP3](locating-the-message-download-history-for-a-pop3-account.md)    
- [Análisis del historial DE UIDL de POP3](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/04/parsing-the-pop3-uidl-history.aspx)
    

