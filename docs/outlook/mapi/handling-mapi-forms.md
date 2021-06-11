---
title: Administrar formularios MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c1589d49-2ebe-48ce-85c7-b70fb7c1bb67
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 91347f0c34b8d7b76e4e456397a1faa061f3b2c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423058"
---
# <a name="handling-mapi-forms"></a>Administrar formularios MAPI

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un formulario MAPI es un visor de un mensaje de una clase determinada. Los clientes que permiten a sus usuarios trabajar con mensajes pertenecientes a una variedad de clases de mensaje deben escribirse para controlar una variedad de formularios MAPI. Para controlar varios formularios, los clientes implementan un componente conocido como visor de formularios que contiene los tres objetos siguientes:
  
- Un objeto de sitio de mensaje, que admite la [interfaz IMAPIMessageSite : IUnknown.](imapimessagesiteiunknown.md) 
    
- Un receptor de aviso de vista, que admite la [interfaz IMAPIViewAdviseSink : IUnknown.](imapiviewadvisesinkiunknown.md) 
    
- Un objeto de contexto de vista, que admite la [interfaz IMAPIViewContext : IUnknown.](imapiviewcontextiunknown.md) 
    
Cada uno de estos objetos lo usa un componente denominado servidor de formularios que implementa cada formulario, controlando su almacenamiento y las notificaciones generadas por los clientes que administran la vista. Otro componente, el proveedor de bibliotecas de formularios, implementa un administrador de formularios. El administrador de formularios administra las bibliotecas de formularios, que almacenan archivos ejecutables del servidor de formularios. Esta administración incluye cargar el servidor de formulario adecuado y controlar la comunicación inicial entre el servidor y el cliente.
  
En el diagrama siguiente se muestra la relación entre un cliente y las demás partes de la arquitectura de formulario MAPI.
  
## <a name="mapi-form-architecture"></a>Arquitectura de formulario MAPI
  
![Arquitectura de formulario MAPI arquitectura]de formulario(media/forms01.gif "MAPI")
  
Si el cliente tiene previsto administrar formularios MAPI, usará la interfaz [IMAPIFormMgr : IUnknown](imapiformmgriunknown.md) del administrador de formularios para realizar cinco tareas básicas: 
  
- Inicie el servidor de formulario MAPI adecuado cuando se abra o compona un mensaje.
    
- Mostrar los iconos de los servidores de formulario en las tablas de contenido de las carpetas.
    
- Enviar y recibir notificaciones de formulario. Para obtener más información, vea [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).
    
- Permitir a los usuarios instalar o quitar servidores de formulario de bibliotecas de formularios. Para obtener más información, vea [Maintaining a Form Library](maintaining-a-form-library.md).
    
- Permitir a los usuarios asociar servidores de formulario con carpetas determinadas.
    
Para obtener acceso al administrador de formularios, llame a la [función MAPIOpenFormMgr](mapiopenformmgr.md) una vez durante la inicialización. 
  
## <a name="in-this-section"></a>En esta sección

- [Implementar un Visor de formularios:](implementing-a-form-viewer.md)describe cómo implementar un visor de formularios mediante un receptor de avisos de vista, un sitio de mensajes y un contexto de vista.
    
- [Implementación de verbos de formulario estándar:](implementing-standard-form-verbs.md)describe cómo implementar los verbos para los clics de botón o menú del usuario en los formularios MAPI.
    
- [Enviar y recibir notificaciones de formulario:](sending-and-receiving-form-notifications.md)describe cómo enviar y recibir notificaciones de formulario.
    
- [Mantenimiento de una biblioteca de formularios:](maintaining-a-form-library.md)describe cómo mantener una biblioteca que contiene toda la información importante sobre un formulario.
    
- [Cargar un mensaje en un formulario:](loading-a-message-into-a-form.md)describe cómo cargar un mensaje en un formulario.
    
- [Redacción de un nuevo mensaje mediante un formulario:](composing-a-new-message-by-using-a-form.md)describe cómo redactar un mensaje mediante un formulario.
    
- [Mostrar iconos de](displaying-form-icons.md)formulario: describe los pasos para mostrar un icono con un formulario.
    
## <a name="see-also"></a>Vea también

- [Formularios MAPI](mapi-forms.md)
- [Desarrollo de servidores de formulario MAPI](developing-mapi-form-servers.md)

