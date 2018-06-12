---
title: Responsabilidades de nomenclatura de cliente
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dbb6ba5f-18c8-426f-9f50-ce6f2fd1dc5b
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: a97d108b2f36b40e5f8818ea81c138d7384ce9b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816557"
---
# <a name="client-naming-responsibilities"></a>Responsabilidades de nomenclatura de cliente

  
  
**Se aplica a**: Outlook 
  
Los clientes deben seguir una convención de nomenclatura para sus propiedades que necesitan ser traducidos por una puerta de enlace. Todas las propiedades que se debe traducir deben crearse como propiedades con nombre en uno de los conjuntos de cinco propiedades designados para contener pueda asignables propiedades:
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
PS_ROUTING_SEARCH_KEY
  
Hacer frente a las propiedades que se relacionan con el mismo usuario debe estar asignado el mismo nombre. Las puertas de enlace se basan en esta convención de nomenclatura, que les permite para que coincida con una dirección con su tipo de dirección correcta. Para analizar la dirección, la asignación entre la dirección y el tipo de dirección debe ser precisa.
  
Con el nombre de las propiedades de MAPI se representan con la estructura de datos **MAPINAMEID** , que especifica que el nombre de la propiedad puede ser una cadena Unicode o un entero de 32 bits. Para obtener más información, vea [MAPINAMEID](mapinameid.md). Entero de nomenclatura se recomienda para los grupos de direcciones porque es una forma sencilla para diferenciar entre conjuntos de propiedades pueda asignables y fácilmente puede servir como un índice para el usuario. La alternativa al uso de números enteros es para asignar una cadena como el nombre de todos los cinco de las propiedades de un usuario pueda asignar. Si sólo hay un usuario requiere asignación, asignación de una cadena es aceptable. Sin embargo, cuando hay varios usuarios, es mejor usar entero de nomenclatura. El nombre, ya sea numérico o basado en la cadena debe almacenarse en una propiedad de específico de la clase de mensaje o en una propiedad que pertenecen a un conjunto de propiedades que se define mediante la aplicación cliente. 
  
> [!NOTE]
> Evitar la traducción de nombres de entero a cadenas, como "route_recipient_1" y "route_recipient_2." No es necesario usar este esfuerzo. 
  
Para ilustrar cómo funciona esta convención de nomenclatura, considere la posibilidad de una aplicación de enrutamiento que envía un mensaje a cada miembro de un equipo de cuatro personas. Cuando un miembro recibe el mensaje, navegará debe responder a él antes de que se pueda enviar junto con las respuestas compiladas hasta el siguiente miembro. El mensaje original contiene una lista de destinatarios con una entrada: el primer miembro del equipo. Incrustados dentro del mensaje son las propiedades pueda asignar la puerta de enlace para los otros tres miembros del equipo. Cada miembro tiene cinco propiedades de usuario principales que residen en los conjuntos de propiedades pueda asignar la puerta de enlace, que se asignan a un número único como un nombre. 
  
En la siguiente tabla ilustra las opciones de configuración para cada conjunto de propiedades pueda asignar la puerta de enlace almacenadas para el resto de los miembros del equipo al que se enruta el mensaje cuando haya terminado con él el primer miembro del equipo de tres.
  
|**Conjunto de propiedades**|**Segundo equipo <br/> miembro**|**En tercer lugar de equipo <br/> miembro**|**Cuarto equipo <br/> miembro**|
|:-----|:-----|:-----|:-----|
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Dirección = 0  <br/> |Dirección = 1  <br/> |Dirección = 2  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Tipo de dirección = 0  <br/> |Tipo de dirección = 1  <br/> |Tipo de dirección = 2  <br/> |
|PS_ROUTING_DISPLAY_NAME  <br/> |Nombre para mostrar = 0  <br/> |Nombre para mostrar = 1  <br/> |Nombre para mostrar = 2  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Identificador de entrada = 0  <br/> |Identificador de entrada = 1  <br/> |Identificador de entrada = 2  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Clave de búsqueda = 0  <br/> |Clave de búsqueda = 1  <br/> |Clave de búsqueda = 2  <br/> |
   
Los clientes que usan las claves de búsqueda pueda asignar como referencias a otras propiedades del mensaje deben reconocer las demás propiedades del mensaje no se traducirá a menos que se colocan en uno de estos conjuntos de propiedades pueda asignar. Cuando se envía un mensaje con ocupa referencias a las claves de búsqueda asignada a un destino en otro dominio de mensajería, las referencias no son válidas. Para habilitar estas otras propiedades para permanecen sincronizadas con las claves de búsqueda, se pueden asignar nombres de cadena en el conjunto de propiedades PS_ROUTING_SEARCH_KEY que no interfieran con los nombres dados a cualquiera de las propiedades pueda asignar principales. Por ejemplo, supongamos que un cliente necesita transmitir una propiedad que contiene la clave de búsqueda para la última persona en una lista de enrutamiento durante cuánto tiempo. El cliente puede crear una propiedad con nombre en el conjunto de propiedades PS_ROUTING_SEARCH_KEY denominado "last_search_key." Debido a que se almacena en un conjunto de propiedades pueda asignar, la propiedad "last_search_key" se traduce junto con el resto de las propiedades que se pueda asignar la puerta de enlace.
  

