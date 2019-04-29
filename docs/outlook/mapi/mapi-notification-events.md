---
title: Eventos de notificación MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ef082d7b-9b2d-4267-beb5-d3ed1d9c7bbf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0d05672a0b136520216357cc85a6b7a125415759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427958"
---
# <a name="mapi-notification-events"></a>Eventos de notificación MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando las aplicaciones cliente se registran para la notificación de eventos, deben especificar uno o más eventos. Los eventos que pueden especificar dependen del conjunto de eventos que admita el origen de notificación correspondiente. Hay diez tipos de notificaciones que los clientes y proveedores de servicios pueden registrarse, cada una de ellas representada por una constante. La notificación de objeto de estado es una excepción. La notificación de objeto de estado es una notificación de MAPI interna; los clientes no pueden registrarse para ti y los proveedores de servicios no pueden generarlos. En la tabla siguiente se describen los tipos de eventos y los objetos de origen de Advise que pueden admitirlos. La constante del evento se incluye con el tipo de evento.
  
|**Tipo de evento**|**Descripción**|**Notificar objetos de origen**|
|:-----|:-----|:-----|
|Error crítico ( _fnevCriticalError_)  <br/> |Se ha producido un error global o un evento, como un cierre de sesión en curso.  <br/> |Sesión, todos los tipos de objetos de la libreta de direcciones y del almacén de mensajes, tabla, estado  <br/> |
|Objeto modificado ( _fnevObjectModified_)  <br/> |Un objeto MAPI ha cambiado.  <br/> |Carpetas, mensajes, todos los tipos de objetos de la libreta de direcciones  <br/> |
|Objeto creado ( _fnevObjectCreated_)  <br/> |Se ha creado un objeto MAPI.  <br/> |Carpetas, mensajes, todos los tipos de objetos de la libreta de direcciones  <br/> |
|Objeto movido ( _fnevObjectMoved_)  <br/> |Se ha movido un objeto MAPI.  <br/> |Carpetas, mensajes, todos los tipos de objetos de la libreta de direcciones  <br/> |
|Objeto eliminado ( _fnevObjectDeleted_)  <br/> |Se ha eliminado un objeto MAPI.  <br/> |Carpetas, mensajes, todos los tipos de objetos de la libreta de direcciones  <br/> |
|Objeto copiado ( _fnevObjectCopied_)  <br/> |Se ha copiado un objeto MAPI.  <br/> |Carpetas, mensajes, todos los tipos de objetos de la libreta de direcciones  <br/> |
|Evento extendido ( _fnevExtended_)  <br/> |Se ha producido un evento interno definido por un proveedor de servicios en particular.  <br/> |Cualquier objeto de origen Advise  <br/> |
|Búsqueda completada ( _fnevSearchComplete_)  <br/> |Una operación de búsqueda ha finalizado y los resultados de la búsqueda están disponibles.  <br/> |Folders  <br/> |
|Tabla modificada ( _fnevTableModified_)  <br/> |La información de un objeto de tabla MAPI ha cambiado.  <br/> |Tablas  <br/> |
|Correo nuevo ( _fnevNewMail_)  <br/> |Un mensaje se ha entregado y está a la espera de ser procesado.  <br/> |Almacén de mensajes, carpetas  <br/> |
   
Un proveedor de servicios define el evento extendido para representar un evento que no puede abarcar otros eventos predefinidos. Solo los clientes que sepan que deben registrarse antes de que un proveedor de servicios admita un evento extendido pueden registrarse para ese evento. Los clientes no pueden determinar sin conocimientos previos si un proveedor de servicios admite un evento extendido y, si es así, cómo controlar dicho evento cuando se recibe.
  

