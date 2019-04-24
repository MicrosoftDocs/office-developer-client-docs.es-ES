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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279698"
---
# <a name="one-off-entry-identifiers"></a>Identificadores de entrada puntuales
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI crea identificadores de entrada de un solo uso en el método **IAddrBook:: CreateOneOff** y en componentes que no tienen acceso al subsistema MAPI, como los componentes de la puerta de enlace. For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md). En la siguiente ilustración se muestra el formato de un identificador de entrada de un solo uso.
  
**Formato de identificador de entrada con definición**
  
![Formato de identificador de entrada de un solo uso] (media/amapi_69.gif "Formato de identificador de entrada de un solo uso")
  
El primer campo es una estructura [MAPIUID](mapiuid.md) especial que identifica el identificador de entrada como representación de un destinatario personalizado. Esta estructura **MAPIUID** debe establecerse en la constante MAPI_ONE_OFF_UID. MAPI_ONE_OFF_UID se define en el archivo de encabezado MAPIDEFS. H. 
  
Los campos version y Flags son palabras de 16 bits en el orden de bytes de Intel. El campo version debe establecerse en cero. El campo flags se puede establecer en los siguientes valores:
  
MAPI_ONE_OFF_NO_RICH_INFO
  
MAPI_ONE_OFF_UNICODE
  
La marca MAPI_ONE_OFF_NO_RICH_INFO se establece si un destinatario no debe recibir el contenido de los mensajes en el formato de encapsulación neutro para el transporte (TNEF). Esta marca se establece cuando MAPI_SEND_NO_RICH_INFO se pasa al método [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) . 
  
La marca MAPI_ONE_OFF_UNICODE se establece si el nombre para mostrar y la dirección de correo electrónico son cadenas Unicode. Esta marca se establece cuando MAPI_UNICODE se pasa a **IAddrBook:: CreateOneOff**. Cuando la marca MAPI_UNICODE no se pasa a **CreateOneOff**, MAPI supone que el nombre para mostrar y las cadenas de dirección de correo electrónico están en el conjunto de caracteres ANSI actual de la estación de trabajo. Por lo general, las cadenas ANSI no funcionan bien en los mensajes que se envían entre plataformas que usan distintos conjuntos de caracteres porque la página de códigos no está codificada en el identificador de entrada. Para protegerse contra esta posible incompatibilidad, muchos tipos de direcciones están limitados a solo los caracteres que son comunes en varios conjuntos de caracteres. Sin embargo, para garantizar la compatibilidad del juego de caracteres y la plataforma, los clientes deben usar Unicode para las cadenas de caracteres en sus mensajes.
  
El nombre para mostrar es una cadena terminada en null que corresponde a la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) del destinatario y al parámetro _LpszName_ que se pasa a **IAddrBook:: CreateOneOff**. El juego de caracteres es Unicode si la marca MAPI_ONE_OFF_UNICODE está configurada y ANSI si está desactivada. 
  
El tipo de dirección es una cadena terminada en null que corresponde a la propiedad **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) del destinatario y al parámetro _lpszAdrType_ pasado a **IAddrBook:: CreateOneOff**. 
  
La dirección de correo electrónico es una cadena terminada en null que corresponde a la propiedad **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) del destinatario y al parámetro _lpszAddress_ pasado a **IAddrBook:: CreateOneOff**. 
  
> [!NOTE]
> No hay relleno en estructuras de identificador de entrada de un solo uso; los bytes se empaquetan exactamente como se indica anteriormente y la longitud del identificador de entrada no debe incluir ningún byte más allá del carácter null de terminación de la dirección de correo electrónico. 
  
Los clientes y los proveedores de libretas de direcciones que construyen manualmente identificadores de entrada de un solo uso también podrían necesitar generar valores para las propiedades **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) y **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). La clave de registro es idéntica al identificador de entrada. La clave de búsqueda se debe formar concatenando los siguientes campos en el orden siguiente:
  
1. El tipo de dirección, convertido a caracteres en mayúsculas.
    
2. Dos puntos (:).
    
3. La dirección de correo electrónico, convertida a caracteres en mayúsculas.
    
4. Un carácter null de terminación.
    
No debe realizarse ninguna conversión del juego de caracteres al generar la clave de búsqueda.
  

