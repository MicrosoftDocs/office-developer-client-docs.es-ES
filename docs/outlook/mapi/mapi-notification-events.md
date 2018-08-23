---
title: Eventos de notificación de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ef082d7b-9b2d-4267-beb5-d3ed1d9c7bbf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8acf197f305373c082ef411732d631535201d488
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567254"
---
# <a name="mapi-notification-events"></a>Eventos de notificación de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando las aplicaciones cliente de registrar la notificación de eventos, deben especificar uno o más eventos. Dependen de los eventos que se pueden especificar en el conjunto de eventos que admite el origen de advise previsto. Hay diez tipos de notificaciones que se pueden registrar los clientes y proveedores de servicios para cada uno de ellos representado por una constante. Notificación de estado de objeto es una excepción. Notificación de estado de objeto es una notificación de MAPI interno; los clientes no se pueden registrar para él y proveedores de servicios lo no pueden generar. En la siguiente tabla se describe los tipos de eventos y los objetos de origen advise que las admiten. La constante de eventos se incluye con el tipo de evento.
  
|**Tipo de evento**|**Descripción**|**Objetos de origen de aviso**|
|:-----|:-----|:-----|
|Error crítico ( _fnevCriticalError_)  <br/> |Se ha producido un error global o evento, como un cierre de sesión en curso.  <br/> |Sesión, todos los tipos de almacén de mensajes y objetos de la libreta de direcciones, tabla, estado  <br/> |
|Objeto modificado ( _fnevObjectModified_)  <br/> |Un objeto MAPI ha cambiado.  <br/> |Las carpetas, los mensajes, todos los tipos de objetos de la libreta de direcciones  <br/> |
|Objeto creado ( _fnevObjectCreated_)  <br/> |Se ha creado un objeto MAPI.  <br/> |Las carpetas, los mensajes, todos los tipos de objetos de la libreta de direcciones  <br/> |
|Objeto que se ha movido ( _fnevObjectMoved_)  <br/> |Se ha movido un objeto MAPI.  <br/> |Las carpetas, los mensajes, todos los tipos de objetos de la libreta de direcciones  <br/> |
|Objeto eliminado ( _fnevObjectDeleted_)  <br/> |Se ha eliminado un objeto MAPI.  <br/> |Las carpetas, los mensajes, todos los tipos de objetos de la libreta de direcciones  <br/> |
|Objeto copiado ( _fnevObjectCopied_)  <br/> |Se ha copiado un objeto MAPI.  <br/> |Las carpetas, los mensajes, todos los tipos de objetos de la libreta de direcciones  <br/> |
|Evento extendida ( _fnevExtended_)  <br/> |Se ha producido un evento interno definido por un proveedor de servicio en particular.  <br/> |Cualquier objeto de origen advise  <br/> |
|Búsqueda completa ( _fnevSearchComplete_)  <br/> |Ha finalizado una operación de búsqueda y los resultados de la búsqueda están disponibles.  <br/> |Folders  <br/> |
|Tabla modificada ( _fnevTableModified_)  <br/> |Ha cambiado la información de un objeto table MAPI.  <br/> |Tablas  <br/> |
|Correo nuevo ( _fnevNewMail_)  <br/> |Un mensaje se ha entregado y se espera de ser procesados.  <br/> |Almacén de mensajes, las carpetas  <br/> |
   
El evento extendido está definido por un proveedor de servicios para representar un evento que no debe estar cubierto por cualquiera de los demás eventos predefinidos. Solo los clientes que saber antes de que registran que un proveedor de servicios admite un evento extendido pueden registrar para dicho evento. No es posible para los clientes determinar sin conocimiento anticipado si un proveedor de servicios admite un evento extendido y, si es así, cómo controlar un evento cuando se recibe.
  

