---
title: Implementar un visor de formularios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bbd0792b0e3e3f274797fabd7f5d5eb49cfc73fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435820"
---
# <a name="implementing-a-form-viewer"></a>Implementar un visor de formularios

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un visor de formularios incluye tres objetos: un sitio de mensajes, un receptor de notificaciones de vista y un contexto de vista. Cada uno de estos objetos permite interactuar con un servidor de formularios y sus formularios.
  
Un sitio de mensaje es un objeto que implementa la interfaz [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) y ayuda a los servidores de formularios con tareas como mover, guardar o eliminar mensajes, crear nuevos mensajes o iniciar nuevos servidores de formularios. Los formularios usan los sitios de mensajes para obtener información sobre el estado del cliente con respecto a varios proveedores de servicios. Por ejemplo, un formulario puede usar el sitio de mensajes para obtener un puntero a su almacén de mensajes actual, un mensaje o una carpeta. 
  
Hay dos tipos de métodos en la interfaz **IMAPIMessageSite** : 
  
- Métodos que proporcionan información a los objetos de formulario.
    
- Métodos que manipulan mensajes.
    
Los métodos que proporcionan información a los objetos de formulario son sencillos de implementar. En todos los casos excepto [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md), ya debe tener disponible la información que necesita cada método.
  
Los métodos que manipulan mensajes deben actuar como si se hubieran desencadenado a través de la interfaz de usuario normal. Por ejemplo, si un objeto de formulario llama al método [IMAPIMessageSite:: NewMessage](imapimessagesite-newmessage.md) , se comportará como si el usuario hubiese elegido redactar un nuevo mensaje personalizado con la interfaz de usuario normal. Los comandos que normalmente generan este comportamiento son **redactar**, **abrir**, **responder**, **responder a todos los destinatarios**y reenviar. **** 
  
Un contexto de vista es un objeto que implementa la interfaz [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) y proporciona a los servidores de formularios un contexto para el mensaje actual, lo que permite a los servidores cambiar fácilmente al mensaje siguiente o anterior de la carpeta. Un formulario usa un contexto de vista para compartir información. Con un objeto de contexto de vista, un formulario puede: 
  
- Regístrese con su cliente para obtener notificaciones.
    
- Activar el mensaje siguiente o anterior de la carpeta.
    
- Obtener información de impresión.
    
- Obtener el estado del cliente.
    
- Obtener una secuencia que se puede usar para guardar la versión de texto de un mensaje.
    
De forma similar a los métodos de la interfaz [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) , los métodos de **IMAPIViewContext** se relacionan con las acciones de usuario y las características de cliente que se relacionan con el contexto de la vista. Por ejemplo, un contexto de vista está implicado en la activación del mensaje siguiente o anterior, la ordenación del contenido de la carpeta y el filtrado del contenido de la carpeta. 
  
No es importante qué mecanismo se proporciona a los usuarios para activar estas características, sólo es importante que la semántica de dichas características se asigne correctamente a los métodos de la interfaz **IMAPIViewContext** . 
  
Un receptor View Advise es un objeto que implementa la interfaz [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) y controla las notificaciones de los servidores de formularios que afectan al visor, y a los formularios y visores de formulario de ayuda para trabajar juntos. Para obtener más información, consulte [enviar y recibir notificaCiones de formulario](sending-and-receiving-form-notifications.md). 
  

