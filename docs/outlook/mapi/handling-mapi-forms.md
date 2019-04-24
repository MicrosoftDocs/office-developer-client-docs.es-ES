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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299457"
---
# <a name="handling-mapi-forms"></a>Administrar formularios MAPI

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un formulario MAPI es un visor para un mensaje de una clase concreta. Los clientes que permiten a los usuarios trabajar con mensajes que pertenecen a una variedad de clases de mensajes deben estar escritos para controlar una variedad de formularios MAPI. Para controlar varios formularios, los clientes implementan un componente conocido como visor de formularios que contiene los tres objetos siguientes:
  
- Un objeto de sitio de mensaje, que admite la interfaz [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) . 
    
- Un receptor de notificación de vista, que admite la interfaz [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) . 
    
- Un objeto de contexto de vista, que admite la interfaz [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) . 
    
Cada uno de estos objetos se usa en un componente denominado servidor de formularios que implementa cada formulario, administrando su almacenamiento y las notificaciones generadas por los clientes que controlan la vista. Un otro componente, el proveedor de la biblioteca de formularios, implementa un administrador de formularios. El administrador de formularios administra las bibliotecas de formularios, que almacenan los archivos ejecutables del servidor de formularios. Esta administración incluye la carga del servidor de formularios apropiado y la administración de la comunicación inicial entre el servidor y el cliente.
  
El siguiente diagrama muestra la relación entre un cliente y las otras partes de la arquitectura de formularios MAPI.
  
## <a name="mapi-form-architecture"></a>Arquitectura de formulario MAPI
  
![Arquitectura de formulario MAPI] (media/forms01.gif "Arquitectura de formulario MAPI")
  
Si el cliente planea controlar los formularios MAPI, usará la interfaz [IMAPIFormMgr: IUnknown](imapiformmgriunknown.md) del administrador de formularios para realizar cinco tareas básicas: 
  
- Inicie el servidor de formularios MAPI adecuado cuando se abra o componga un mensaje.
    
- Mostrar iconos de servidores de formulario en las tablas de contenido de las carpetas.
    
- Enviar y recibir notificaciones de formulario. Para obtener más información, consulte [enviar y recibir notificaCiones de formulario](sending-and-receiving-form-notifications.md).
    
- Permitir a los usuarios instalar o quitar servidores de formularios de las bibliotecas de formularios. Para obtener más información, vea [mantener una biblioteca de formularios](maintaining-a-form-library.md).
    
- Permitir a los usuarios asociar servidores de formularios con carpetas específicas.
    
Para tener acceso al administrador de formularios, llame a la función [MAPIOpenFormMgr](mapiopenformmgr.md) una vez durante la inicialización. 
  
## <a name="in-this-section"></a>En esta sección

- [Implementar un visor de formularios](implementing-a-form-viewer.md): describe cómo implementar un visor de formularios mediante un receptor de vista notificar, un sitio de mensaje y un contexto de vista.
    
- [Implementar verbos de formulario estándar](implementing-standard-form-verbs.md): describe cómo implementar los verbos para los clics de menús o menús de usuario en formularios MAPI.
    
- [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md): describe cómo enviar y recibir notificaciones de formulario.
    
- [Mantenimiento de una biblioteca de formularios](maintaining-a-form-library.md): describe cómo mantener una biblioteca que contiene toda la información importante sobre un formulario.
    
- [Cargar un mensaje en un formulario](loading-a-message-into-a-form.md): describe cómo cargar un mensaje en un formulario.
    
- [Redactar un nuevo mensaje usando un formulario](composing-a-new-message-by-using-a-form.md): describe cómo redactar un mensaje con un formulario.
    
- [Mostrar iconos de formulario](displaying-form-icons.md): describe los pasos para mostrar un icono con un formulario.
    
## <a name="see-also"></a>Vea también

- [Formularios MAPI](mapi-forms.md)
- [Desarrollar servidores de formulario MAPI](developing-mapi-form-servers.md)

