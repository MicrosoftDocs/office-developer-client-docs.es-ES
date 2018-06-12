---
title: Implementación de un visor de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 645f98342b4b3ec2bebf3f233f719bd5cae69da9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817659"
---
# <a name="implementing-a-form-viewer"></a>Implementación de un visor de formulario

  
  
**Se aplica a**: Outlook 
  
Un visor de formulario incluye tres objetos: un sitio de mensaje, una vista de aviso receptor y un contexto de vista. Cada uno de estos objetos permite interactuar con un servidor de formulario y sus formularios.
  
Un sitio de mensaje es un objeto que implementa el [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) de la interfaz y ayuda a los servidores de formulario con las tareas, como mover, guardar o eliminar mensajes, creación de nuevos mensajes o iniciar nuevos servidores de formulario. Sitios de mensaje se usan los formularios para obtener información acerca del estado de su cliente con respecto a varios proveedores de servicios. Por ejemplo, un formulario puede usar el sitio de mensaje para obtener un puntero a su almacén de mensajes actual, un mensaje o una carpeta. 
  
Hay dos tipos de métodos en la interfaz de **IMAPIMessageSite** : 
  
- Métodos que proporcionan información a los objetos de formulario.
    
- Métodos que manipulan los mensajes.
    
Los métodos que proporcionan información a los objetos de formulario son sencillos de implementar. En todos los casos excepto [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), debe tener disponible la información necesaria en cada método.
  
Los métodos que manipulan mensajes deben actuar como si hubiera desencadenado a través de la interfaz de usuario normal. Por ejemplo, si un objeto de formulario llama al método [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) , se comportan como si el usuario ha elegido redactar un nuevo mensaje personalizado con la interfaz de usuario normal. Los comandos que suelen generan este comportamiento son **redacción**, **Abrir**, **responder**, **responder a todos los destinatarios**y **hacia delante**. 
  
Un contexto de vista es un objeto que implementa el [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) de la interfaz y proporciona servidores de formulario con un contexto para el mensaje actual, lo que permite a los servidores cambiar fácilmente al mensaje siguiente o anterior en la carpeta. Un formulario, utiliza un contexto de vista para compartir información. Con un objeto de contexto de vista, un formulario puede: 
  
- Registrar con su cliente para las notificaciones.
    
- Activar el mensaje siguiente o anterior en la carpeta.
    
- Obtenga información de impresión.
    
- Obtener el estado de su cliente.
    
- Obtener una secuencia que se puede usar para guardar la versión de texto de un mensaje.
    
Similar a los métodos en el [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) interfaz, los métodos en **IMAPIViewContext** correlacionan con las acciones del usuario y las características de cliente que se relacionan con el contexto de vista. Por ejemplo, un contexto de vista consiste en activar el mensaje siguiente o anterior, ordenar el contenido de la carpeta y filtrar el contenido de la carpeta. 
  
No es importante qué mecanismo de proporcionar a los usuarios para activar estas características, solo es importante que la semántica de esas características se asigna a los métodos en la interfaz de **IMAPIViewContext** . 
  
Una vista de aviso receptor es un objeto que implementa el [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) interfaz y controladores de notificaciones desde servidores de formulario que afectan a la Ayuda y el Visor de formularios y los visores de formulario para que trabajen conjuntamente. Para obtener más información, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md). 
  

