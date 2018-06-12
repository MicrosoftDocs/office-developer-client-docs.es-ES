---
title: Identificadores de entrada único
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 1335de3c1decf6c594f0148fbbf055061d7ce7e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818424"
---
# <a name="one-off-entry-identifiers"></a>Identificadores de entrada único
  
**Se aplica a**: Outlook 
  
Identificadores de entrada único se crean mediante MAPI en el método **IAddrBook::CreateOneOff** y los componentes que no disponen de acceso en el subsistema MAPI, como los componentes de la puerta de enlace. For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md). En la siguiente ilustración muestra el formato de un identificador de entrada único.
  
**Formato de identificador de entrada único**
  
![Formato de identificador de entrada único] (media/amapi_69.gif "Formato de identificador de entrada único")
  
El primer campo es una estructura [MAPIUID](mapiuid.md) especial que identifica el identificador de entrada como que representa un destinatario personalizado. Esta estructura **MAPIUID** debe establecerse en la constante MAPI_ONE_OFF_UID. MAPI_ONE_OFF_UID se define en el archivo de encabezado MAPIDEFS. H. 
  
Los campos de la versión y los indicadores son palabras de 16 bits en orden de bytes de Intel. El campo versión debe establecerse en cero. El campo de indicadores se puede establecer en los siguientes valores:
  
MAPI_ONE_OFF_NO_RICH_INFO
  
MAPI_ONE_OFF_UNICODE
  
Si un destinatario debe recibir el contenido del mensaje en el formato de encapsulación neutro de transporte (TNEF), se establece la marca MAPI_ONE_OFF_NO_RICH_INFO. Este indicador se establece cuando MAPI_SEND_NO_RICH_INFO se pasa al método [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) . 
  
Si la dirección de correo electrónico y de nombre para mostrar es cadenas Unicode, se establece la marca MAPI_ONE_OFF_UNICODE. Este indicador se establece cuando se pasa la MAPI_UNICODE **IAddrBook::CreateOneOff**. Cuando no se pasa el indicador MAPI_UNICODE **CreateOneOff**, MAPI se supone que las cadenas de dirección para mostrar, nombre y correo electrónico se encuentran en el juego de caracteres ANSI actual de la estación de trabajo. Cadenas ANSI generalmente no funcionan bien en los mensajes que se envían entre plataformas que utilizan diferentes conjuntos de caracteres porque la página de códigos no está codificada en el identificador de entrada. Para proteger contra esta incompatibilidad posible, muchos tipos de direcciones se limitan a sólo los caracteres que son comunes a varios conjuntos de caracteres. Sin embargo, para garantizar la compatibilidad de plataforma y conjunto de caracteres, los clientes deben usar Unicode para las cadenas de caracteres en sus mensajes.
  
El nombre para mostrar es una cadena terminada en null que corresponde a la propiedad del destinatario **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y para el parámetro _lpszName_ pasadas a **IAddrBook::CreateOneOff**. El juego de caracteres es Unicode si la marca MAPI_ONE_OFF_UNICODE es conjunto y ANSI si está claro. 
  
El tipo de dirección es una cadena terminada en null que corresponde a la propiedad del destinatario **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) y para el parámetro _lpszAdrType_ pasadas a **IAddrBook::CreateOneOff**. 
  
La dirección de correo electrónico es una cadena terminada en null que corresponde a la propiedad del destinatario **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) y para el parámetro _lpszAddress_ pasadas a **IAddrBook::CreateOneOff**. 
  
> [!NOTE]
> No hay ningún relleno en las estructuras de identificador de entrada único; los bytes se empaquetan exactamente como se indicó anteriormente y la longitud del identificador de entrada no debe incluir cualquier bytes más allá del carácter null de terminación de la dirección de correo electrónico. 
  
Los clientes y los proveedores de la libreta de direcciones que construcción manualmente los identificadores de entrada único también es posible que necesite generar valores para las propiedades de **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) y **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). La clave de registro es idéntica al valor del identificador de entrada. La clave de búsqueda debe se forma concatenando los siguientes campos en el orden siguiente:
  
1. El tipo de dirección, convertido a caracteres en mayúsculas.
    
2. Un carácter de dos puntos (:).
    
3. La dirección de correo electrónico, se convierten en caracteres en mayúsculas.
    
4. Un carácter nulo.
    
Conversión del conjunto de caracteres no debe realizarse al generar la clave de búsqueda.
  

