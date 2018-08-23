---
title: Control de formularios MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c1589d49-2ebe-48ce-85c7-b70fb7c1bb67
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c6cdb07e1cbe68d90c6dcd9d5418f700ea5abc3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589654"
---
# <a name="handling-mapi-forms"></a>Control de formularios MAPI

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un formulario MAPI es un visor para un mensaje de una clase determinada. Los clientes que permiten a los usuarios a trabajar con los mensajes que pertenecen a una variedad de clases de mensaje deben escribirse para controlar una gran variedad de formularios MAPI. Para controlar varios formularios, los clientes de implementan un componente conocido como un visor de formulario que contiene los siguientes tres objetos:
  
- Un objeto de sitio de mensaje, que es compatible con la [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) interfaz. 
    
- Una vista de aviso receptor, que es compatible con la [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) interfaz. 
    
- Un objeto de contexto de vista, que admite la [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) interfaz. 
    
Cada uno de estos objetos se usa en un componente denominado servidor de formulario que implementa cada control de formularios, su almacenamiento de información y las notificaciones generadas por la vista de gestión de los clientes. Uno de otro componente, el proveedor de biblioteca de formulario, implementa el Administrador de un formulario. El Administrador de formularios administra las bibliotecas de formulario, que almacenan los archivos ejecutables del servidor de formulario. Esta administración incluye al cargar el servidor de forma adecuada y controlar la comunicación inicial entre el servidor y el cliente.
  
En el siguiente diagrama se muestra la relación entre un cliente y las demás partes de la arquitectura de formulario MAPI.
  
## <a name="mapi-form-architecture"></a>Arquitectura de formulario MAPI
  
![Arquitectura de formulario MAPI] (media/forms01.gif "Arquitectura de formulario MAPI")
  
Si los planes de su cliente administrar los formularios MAPI, va a usar el Administrador de formulario [IMAPIFormMgr: IUnknown](imapiformmgriunknown.md) interfaz para realizar las cinco tareas básicas: 
  
- Inicie el servidor de formulario MAPI adecuado cuando se abre o se compone un mensaje.
    
- Mostrar los iconos de los servidores de formulario en las tablas de contenido de carpetas.
    
- Enviar y recibir notificaciones de formulario. Para obtener más información, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).
    
- Permitir a los usuarios instalar o quitar servidores de formulario de las bibliotecas de formularios. Para obtener más información, consulte [Mantenimiento de una biblioteca de formularios](maintaining-a-form-library.md).
    
- Permitir a los usuarios asociar los servidores de formulario a determinadas carpetas.
    
Para tener acceso al administrador de formulario, llame a la función [MAPIOpenFormMgr](mapiopenformmgr.md) una vez durante la inicialización. 
  
## <a name="in-this-section"></a>En esta sección

- [Implementación de un visor de formulario](implementing-a-form-viewer.md): describe cómo implementar un visor de formulario mediante el uso de una vista de aviso receptor, un sitio de mensaje y un contexto de vista.
    
- [Implementación de verbos estándar de formulario](implementing-standard-form-verbs.md): describe cómo implementar los verbos para clics de menú o botón de usuario en los formularios MAPI.
    
- [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md): se describe cómo enviar y recibir notificaciones de formulario.
    
- [Mantenimiento de una biblioteca de formularios](maintaining-a-form-library.md): describe cómo mantener una biblioteca que contiene toda la información importante acerca de un formulario.
    
- [Carga de un mensaje en un formulario](loading-a-message-into-a-form.md): describe cómo cargar un mensaje en un formulario.
    
- [Redactar un nuevo mensaje mediante el uso de un formulario](composing-a-new-message-by-using-a-form.md): describe cómo se redacta un mensaje mediante un formulario.
    
- [Mostrar iconos de formulario](displaying-form-icons.md): se describen los pasos para mostrar un icono con un formulario.
    
## <a name="see-also"></a>Recursos adicionales

- [Formularios MAPI](mapi-forms.md)
- [Desarrollar servidores de formulario MAPI](developing-mapi-form-servers.md)

