---
title: Responsabilidades de nomenclatura de clientes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dbb6ba5f-18c8-426f-9f50-ce6f2fd1dc5b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 808c7abf3d29872a8c5095fdc6dc39b2107a8993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424955"
---
# <a name="client-naming-responsibilities"></a>Responsabilidades de nomenclatura de clientes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes deben seguir una convención de nomenclatura para sus propiedades que deben traducirse mediante una puerta de enlace. Todas las propiedades que se traducirán deben crearse como propiedades con nombre en uno de los cinco conjuntos de propiedades designados para contener propiedades asignables:
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
PS_ROUTING_SEARCH_KEY
  
Las propiedades de direccionamiento relacionadas con el mismo usuario deben tener el mismo nombre. Las puertas de enlace dependen de esta convención de nomenclatura, que les permite hacer coincidir una dirección con su tipo de dirección correcto. Para el análisis de direcciones, la asignación entre la dirección y el tipo de dirección debe ser precisa.
  
Las propiedades con nombre MAPI se representan con la estructura de datos **MAPINAMEID,** que especifica que el nombre de la propiedad puede ser una cadena Unicode o un entero de 32 bits. Para obtener más información, vea [MAPINAMEID](mapinameid.md). La nomenclatura de enteros se recomienda para grupos de direcciones porque es una forma sencilla de diferenciar entre conjuntos de propiedades asignables y puede servir fácilmente como un índice para el usuario. La alternativa al uso de enteros es asignar una cadena como el nombre de las cinco propiedades asignables de un usuario. Si solo un usuario requiere asignación, la asignación de una cadena es aceptable. Sin embargo, cuando hay varios usuarios, es mejor usar la nomenclatura de enteros. El nombre, ya sea numérico o basado en cadenas, debe almacenarse en una propiedad específica de clase de mensaje o en una propiedad perteneciente a un conjunto de propiedades definido por la aplicación cliente. 
  
> [!NOTE]
> Evite traducir nombres enteros a cadenas, como "route_recipient_1" y "route_recipient_2". Este esfuerzo no es necesario. 
  
Para ilustrar cómo funciona esta convención de nomenclatura, considere la posibilidad de usar una aplicación de enrutamiento que envíe un mensaje a cada miembro de un equipo de cuatro personas. Cuando un miembro recibe el mensaje, debe responderlo antes de que se pueda enviar junto con las respuestas compiladas al siguiente miembro. El mensaje original contiene una lista de destinatarios con una entrada: el primer miembro del equipo. Las propiedades asignadas a la puerta de enlace de los otros tres miembros del equipo están incrustadas en el mensaje. Cada miembro tiene cinco propiedades de usuario principales que residen en los conjuntos de propiedades asignables a la puerta de enlace, a las que se asigna un número único como nombre. 
  
En la tabla siguiente se muestra la configuración de cada conjunto de propiedades asignables de puerta de enlace almacenadas para los tres miembros del equipo restantes a los que se enruta el mensaje cuando el primer integrante del equipo termina con él.
  
|**Propiedad Set**|**Segundo integrante del  <br/> equipo**|**Tercer integrante del  <br/> equipo**|**Fourth Team  <br/> Member**|
|:-----|:-----|:-----|:-----|
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Dirección = 0  <br/> |Dirección = 1  <br/> |Dirección = 2  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Tipo de dirección = 0  <br/> |Tipo de dirección = 1  <br/> |Tipo de dirección = 2  <br/> |
|PS_ROUTING_DISPLAY_NAME  <br/> |Nombre para mostrar = 0  <br/> |Nombre para mostrar = 1  <br/> |Nombre para mostrar = 2  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Identificador de entrada = 0  <br/> |Identificador de entrada = 1  <br/> |Identificador de entrada = 2  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Clave de búsqueda = 0  <br/> |Clave de búsqueda = 1  <br/> |Clave de búsqueda = 2  <br/> |
   
Los clientes que usan claves de búsqueda asignables como referencias a otras propiedades de mensaje deben reconocer que las demás propiedades del mensaje no se traducirán a menos que se coloquen en uno de estos conjuntos de propiedades asignables. Cuando se envía un mensaje con referencias sin asignar a claves de búsqueda asignadas a un destino en otro dominio de mensajería, las referencias no son válidas. Para permitir que estas otras propiedades permanezcan sincronizadas con las claves de búsqueda, puede asignarles nombres de cadena en el conjunto de propiedades de PS_ROUTING_SEARCH_KEY que no interfieran con los nombres asignados a ninguna de las propiedades asignables principales. Por ejemplo, supongamos que un cliente debe transmitir una propiedad que contenga la clave de búsqueda de la última persona de una lista de enrutamiento larga. El cliente puede crear una propiedad con nombre en el PS_ROUTING_SEARCH_KEY de propiedades denominada "last_search_key". Dado que se almacena en un conjunto de propiedades asignables, la propiedad "last_search_key" se traduce junto con el resto de las propiedades asignables a la puerta de enlace.
  

