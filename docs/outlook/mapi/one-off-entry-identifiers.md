---
title: Identificadores de entrada puntuales
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: abe52cb45e13e6713d28fffe379e245e2483bffa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411046"
---
# <a name="one-off-entry-identifiers"></a>Identificadores de entrada puntuales
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI crea los identificadores de entrada de uso único en el método **IAddrBook::CreateOneOff** y los componentes que no tienen acceso al subsistema MAPI, como los componentes de puerta de enlace. For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md). En la siguiente ilustración se muestra el formato de un identificador de entrada de uso único.
  
**Formato de identificador de entrada con definición**
  
![Formato de identificador de entrada de un solo]acceso formato de identificador de entrada de un solo(media/amapi_69.gif "acceso")
  
El primer campo es una estructura [MAPIUID](mapiuid.md) especial que identifica el identificador de entrada como que representa un destinatario personalizado. Esta **estructura MAPIUID** debe establecerse en la constante MAPI_ONE_OFF_UID. MAPI_ONE_OFF_UID se define en el archivo de encabezado MAPIDEFS.H. 
  
Los campos de versión y marcas son palabras de 16 bits en orden de bytes intel. El campo de versión debe establecerse en cero. El campo de marcas se puede establecer en los siguientes valores:
  
MAPI_ONE_OFF_NO_RICH_INFO
  
MAPI_ONE_OFF_UNICODE
  
La MAPI_ONE_OFF_NO_RICH_INFO se establece si un destinatario no debe recibir el contenido del mensaje en el formato de encapsulación neutro para el transporte (TNEF). Esta marca se establece cuando MAPI_SEND_NO_RICH_INFO se pasa al [método IAddrBook::CreateOneOff.](iaddrbook-createoneoff.md) 
  
El MAPI_ONE_OFF_UNICODE marca se establece si el nombre para mostrar y la dirección de correo electrónico son cadenas Unicode. Esta marca se establece cuando el MAPI_UNICODE se pasa a **IAddrBook::CreateOneOff**. Cuando no MAPI_UNICODE marca a **CreateOneOff**, MAPI supone que las cadenas de nombre para mostrar y dirección de correo electrónico están en el juego de caracteres ANSI actual de la estación de trabajo. Por lo general, las cadenas ANSI no funcionan bien en los mensajes que se envían entre plataformas mediante conjuntos de caracteres diferentes porque la página de códigos no está codificada en el identificador de entrada. Para protegerse contra esta posible incompatibilidad, muchos tipos de direcciones están limitados solo a los caracteres que son comunes en varios conjuntos de caracteres. Sin embargo, para garantizar la compatibilidad del juego de caracteres y la plataforma, los clientes deben usar Unicode para las cadenas de caracteres de sus mensajes.
  
El nombre para mostrar es una cadena terminada en null que corresponde **a** la propiedad PR_DISPLAY_NAME ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) del destinatario y al parámetro  _lpszName_ pasado a **IAddrBook::CreateOneOff**. El juego de caracteres es Unicode si se MAPI_ONE_OFF_UNICODE marca y ANSI si está claro. 
  
El tipo de dirección es una cadena terminada en null que corresponde a la propiedad **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) del destinatario y al parámetro  _lpszAdrType_ pasado a **IAddrBook::CreateOneOff**. 
  
La dirección de correo electrónico es una cadena terminada en null que corresponde a la propiedad **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) del destinatario y al parámetro  _lpszAddress_ pasado a **IAddrBook::CreateOneOff**. 
  
> [!NOTE]
> No hay relleno en las estructuras de identificador de entrada de un solo elemento; los bytes se empaquetan exactamente como se indicó anteriormente y la longitud del identificador de entrada no debe incluir ningún bytes más allá del carácter nulo de terminación de la dirección de correo electrónico. 
  
Los clientes y proveedores de libretas de direcciones que crean manualmente identificadores de entrada de uso único también pueden necesitar generar valores para las propiedades **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) y **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). La clave de registro es idéntica al identificador de entrada. La clave de búsqueda debe formarse concatenando los siguientes campos en el orden siguiente:
  
1. Tipo de dirección, convertido a caracteres en mayúsculas.
    
2. Dos puntos (:).
    
3. La dirección de correo electrónico, convertida en caracteres en mayúsculas.
    
4. Carácter nulo de terminación.
    
No se debe realizar ninguna conversión de juego de caracteres al generar la clave de búsqueda.
  

