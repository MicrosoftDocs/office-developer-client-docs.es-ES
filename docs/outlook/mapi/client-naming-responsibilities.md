---
title: Responsabilidades de nombres de cliente
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
# <a name="client-naming-responsibilities"></a>Responsabilidades de nombres de cliente

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes deben seguir una Convención de nomenclatura para sus propiedades que deben traducirse por una puerta de enlace. Todas las propiedades que se van a traducir deben crearse como propiedades con nombre en uno de los cinco conjuntos de propiedades designados para mantener las propiedades asignables:
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
PS_ROUTING_SEARCH_KEY
  
Se debe asignar el mismo nombre a las propiedades de direccionamiento relacionadas con el mismo usuario. Las puertas de enlace dependen de esta Convención de nomenclatura, lo que les permite hacer coincidir una dirección con su tipo de dirección correcto. Para el análisis de direcciones, la asignación entre la dirección y el tipo de dirección debe ser precisa.
  
Las propiedades MAPI con nombre se representan con la estructura de datos **MAPINAMEID** , que especifica que el nombre de la propiedad puede ser una cadena Unicode o un entero de 32 bits. Para obtener más información, vea [MAPINAMEID](mapinameid.md). La nomenclatura de enteros se recomienda para grupos de direcciones porque es una forma sencilla de distinguir entre conjuntos de propiedades asignables, y puede servir fácilmente como un índice para el usuario. La alternativa al uso de enteros es asignar una cadena como nombre a las cinco de las propiedades asignables de un usuario. Si sólo un usuario requiere la asignación, es aceptable asignar una cadena. Sin embargo, cuando hay varios usuarios, es mejor usar nombres enteros. El nombre, ya sea numérico o basado en cadena, debe almacenarse en una propiedad específica de la clase de mensaje o en una propiedad perteneciente a un conjunto de propiedades definido por la aplicación cliente. 
  
> [!NOTE]
> Evite traducir nombres enteros a cadenas, como "route_recipient_1" y "route_recipient_2". Este esfuerzo no es necesario. 
  
Para ilustrar cómo funciona esta Convención de nomenclatura, considere una aplicación de enrutamiento que envíe un mensaje a cada miembro de un equipo de cuatro personas. Cuando un miembro recibe el mensaje, debe responder a él antes de que se pueda enviar junto con las respuestas compiladas al siguiente miembro. El mensaje original contiene una lista de destinatarios con una entrada: el primer integrante del equipo. La incrustación dentro del mensaje son las propiedades asignables a la puerta de enlace para los otros tres miembros del equipo. Cada miembro tiene cinco propiedades de usuario principales que residen en los conjuntos de propiedades asignables de la puerta de enlace, a los que se asigna un número único como nombre. 
  
En la tabla siguiente se muestra la configuración de cada conjunto de propiedades asignables a la puerta de enlace almacenadas para los tres miembros del equipo restantes a quienes se redirige el mensaje cuando el primer miembro del equipo termina con él.
  
|**Propiedad Set**|**Segundo miembro <br/> del equipo**|**Miembro del <br/> tercer equipo**|**Cuarto integrante del grupo <br/>**|
|:-----|:-----|:-----|:-----|
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Dirección = 0  <br/> |Dirección = 1  <br/> |Dirección = 2  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Tipo de dirección = 0  <br/> |Tipo de dirección = 1  <br/> |Tipo de dirección = 2  <br/> |
|PS_ROUTING_DISPLAY_NAME  <br/> |Nombre para mostrar = 0  <br/> |Nombre para mostrar = 1  <br/> |Nombre para mostrar = 2  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Identificador de entrada = 0  <br/> |Identificador de entrada = 1  <br/> |Identificador de entrada = 2  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Clave de búsqueda = 0  <br/> |Clave de búsqueda = 1  <br/> |Clave de búsqueda = 2  <br/> |
   
Los clientes que usan claves de búsqueda asignables como referencias a otras propiedades del mensaje deben reconocer que las otras propiedades del mensaje no se traducirán a menos que se coloquen en uno de estos conjuntos de propiedades asignables. Cuando se envía un mensaje con referencias sin asignar a claves de búsqueda asignadas a un destino en otro dominio de mensajería, las referencias no son válidas. Para permitir que estas otras propiedades permanezcan sincronizadas con las claves de búsqueda, puede asignarles nombres de cadena en el conjunto de propiedades PS_ROUTING_SEARCH_KEY que no interferirán con los nombres dados a ninguna de las principales propiedades asignables. Por ejemplo, supongamos que un cliente debe transmitir una propiedad que contiene la clave de búsqueda de la última persona en una lista de enrutamiento larga. El cliente puede crear una propiedad con nombre en el conjunto de propiedades PS_ROUTING_SEARCH_KEY denominado "last_search_key". Dado que se almacena en un conjunto de propiedades asignables, la propiedad "last_search_key" se traduce junto con el resto de las propiedades asignables a la puerta de enlace.
  

