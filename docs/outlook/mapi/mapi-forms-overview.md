---
title: Introducción a los formularios MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4e7d48f6f6a47ce28aa0e1291ccef209b998c18e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432523"
---
# <a name="mapi-forms-overview"></a>Introducción a los formularios MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un formulario MAPI es un visor de un mensaje. Cada mensaje tiene una clase de mensaje que determina el formulario concreto que se usa como visor. MAPI define varias clases de mensajes y ha implementado los formularios para ver los mensajes de estas clases. Los desarrolladores de software cliente pueden crear nuevas clases de mensajes y formularios personalizados para ver los mensajes creados mediante las nuevas clases.
  
Cada formulario personalizado implementa un conjunto de comandos de menú estándar, como **Abrir** **,** Crear **,** Eliminar y **Responder,** y un conjunto de comandos específicos del formulario en particular. Algunos de los comandos de formulario se integran con la interfaz de usuario de la aplicación cliente cuando el formulario está activo; otros comandos de formulario reemplazan completamente los comandos de cliente. 
  
En la siguiente ilustración se muestra la relación entre los componentes MAPI implicados en el uso de formularios. 
  
**Arquitectura de formulario MAPI**
  
![Arquitectura de formulario]MAPI de arquitectura(media/forms01.gif "de formulario MAPI")
  
En el diagrama, observe que el administrador de formularios desempeña un rol similar a otros proveedores de servicios MAPI, aunque no es un proveedor de servicios en sí. El administrador de formularios es un ARCHIVO DLL reemplazable que implementa algunas de las interfaces MAPI. Aunque los programadores pueden implementar su propio administrador de formularios, la mayoría de los entornos usarán el administrador de formularios proporcionado por Microsoft debido a la complejidad del administrador de formularios.
  
En la siguiente lista se describen los componentes del diagrama y su relación con otros componentes:
  
- Cliente de mensajería: una aplicación que puede usar objetos de formulario. El cliente de mensajería usa las interfaces de formulario MAPI para comunicarse con el administrador de formularios para cargar mensajes en objetos de formulario.
    
- Interfaces de formulario MAPI: un estándar definido para la comunicación entre componentes MAPI relacionados con formularios.
    
- Administrador de formularios: dll que los clientes de mensajería usan para controlar la instalación de formularios en bibliotecas de formularios, la carga de servidores de formularios y la comunicación inicial entre clientes de mensajería y servidores de formularios.
    
- Bibliotecas de formularios: almacenamiento permanente para los archivos ejecutables asociados con servidores de formulario.
    
- Servidores de formulario: archivos ejecutables que implementan un formulario. Los servidores de formularios crean objetos de formulario e interfaces de usuario para tratar mensajes específicos. Este ejecutable también es un servidor OLE y se adhiere a las convenciones OLE habituales.
    
- Objetos de formulario: objetos en tiempo de ejecución creados por servidores de formulario que corresponden a mensajes específicos. Los objetos de formulario se ejecutan en el mismo contexto de proceso que su servidor de formulario.
    
Para obtener más información acerca de los componentes de formulario MAPI, vea [Formularios MAPI](mapi-forms.md).
  
## <a name="see-also"></a>Consulte también

- [Arquitectura y características mapi](mapi-features-and-architecture.md)

