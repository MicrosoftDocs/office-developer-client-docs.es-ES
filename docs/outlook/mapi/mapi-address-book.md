---
title: Libreta de direcciones MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6703ba3f-54a5-4059-b10a-1d42a9e81be1
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 14f9bff8dbf55456c37e70e1ae7a0c236471b6c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298120"
---
# <a name="mapi-address-book"></a>Libreta de direcciones MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La libreta de direcciones integrada es un objeto que implementa MAPI para proporcionar acceso a un conjunto integrado de informaci�n de direcciones de todos los proveedores de libreta de direcciones en el perfil. Con la libreta de direcciones, los proveedores de servicios y las aplicaciones cliente no es necesario diferenciar entre los esquemas de direccionamiento �nicos de sistemas de mensajer�a. En su lugar, puede buscar las direcciones de los destinatarios en cualquier sistema de mensajer�a, siempre y cuando se instala el proveedor de libreta de direcciones para el sistema de mensajer�a.
  
La libreta de direcciones puede tener acceso mediante programaci�n, sin intervenci�n del usuario, o de forma interactiva mediante el uso de cuadros de di�logo comunes. MAPI incluye cuadros de di�logo para mostrar una lista resumida de las entradas en la libreta de direcciones, informaci�n detallada acerca de un destinatario concreto, una advertencia cuando un usuario crea un destinatario que no se puede asignar a una direcci�n �nica y un conjunto de formularios de plantilla para la creaci�n de nuevos destinatarios.
  
La libreta de direcciones MAPI es una estructura similar a un almac�n de mensajes en que se organiza jer�rquicamente. La libreta de direcciones proporciona acceso a tres tipos de objetos implementados por un proveedor de libreta de direcciones:
  
- Un objeto de contenedor de libreta de direcciones.
    
- Un objeto de lista de distribuci�n.
    
- Un objeto de usuario de mensajer�a.
    
Cada uno de estos tipos de objetos se tiene acceso a trav�s de su identificador de entrada �nico asignado por su proveedor de libreta de direcciones. 
  
Contenedores de libretas de direcciones son similares a las carpetas que contienen objetos de distintos tipos. Un contenedor de libreta de direcciones puede contener otros contenedores de libretas de direcciones, as� como los objetos de lista de distribuci�n de mensajer�a. Contenedores de libretas de direcciones se utilizan para organizar y almacenar objetos de libreta de direcciones.
  
Para lograr la apariencia de la libreta de direcciones integrada, los proveedores de libreta de direcciones exponen cero, uno o varios de sus contenedores de nivel superior a MAPI que combina y muestra los resultados en un �nico contenedor de nivel superior. Pueden elegir los proveedores de libreta de direcciones exponer un conjunto de contenedores para un tipo de sesi�n y un conjunto diferente de mensajer�a para otra sesi�n. Tambi�n es posible que los proveedores de libreta de direcciones no tener ning�n contenedores de nivel superior y exponer s�lo una lista de plantillas que se pueden usar para crear a los destinatarios.
  
Destinatarios del mensaje se implementan con el usuario de mensajer�a y objetos de la lista de distribuci�n. Los usuarios de mensajer�a son destinatarios individuales; listas de distribuci�n son los destinatarios del grupo. Cada usuario de mensajer�a tiene una direcci�n �nica de un tipo determinado controlado por un sistema de mensajer�a determinado. Una lista de distribuci�n es una colecci�n con nombre de los destinatarios. Listas de distribuci�n pueden contener objetos de usuario de mensajer�a y otras listas de distribuci�n. Cuando un usuario de una aplicaci�n cliente env�a un mensaje a una lista de distribuci�n, el mensaje se que se env�a a cada uno de los miembros de usuarios de mensajer�a de la lista. 
  
Los usuarios de mensajer�a y listas de distribuci�n tienen un conjunto de cinco propiedades que se conocen como las propiedades de la direcci�n base. Estas son las propiedades necesarias y se describen brevemente los siguientes.
  
|**Propiedad de direcci�n base**|**Description**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Tipo de direcci�n del destinatario. Cada tipo de direcci�n sigue un formato determinado y se usa con un sistema de mensajer�a determinado.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Nombre para mostrar para el destinatario.  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Direcci�n del destinatario.  <br/> |
|**** Es ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Identificador de entrada utilizado para tener acceso al destinatario.  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Binario comparable clave que se usa para identificar al destinatario.  <br/> |
   
MAPI define muchos grupos de propiedades que son variantes de las propiedades de la direcci�n base. Estos otros grupos describen los usuarios de mensajer�a y listas de distribuci�n en diferentes situaciones. Por ejemplo, un grupo de propiedades describe el remitente de delegado de un mensaje y el destinatario de delegado de otro grupo.
  

