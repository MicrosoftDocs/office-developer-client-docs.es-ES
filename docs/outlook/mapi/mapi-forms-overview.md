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
ms.openlocfilehash: 91bc0641723a92d8dc86bf3d1037d8e9936930ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818132"
---
# <a name="mapi-forms-overview"></a>Introducción a los formularios MAPI
  
**Hace referencia a**: Outlook 
  
Un formulario MAPI es un visor para un mensaje. Cada mensaje tiene una clase de mensaje que determina la forma concreta que se usa como su visor. MAPI define varias clases de mensaje y ha implementado los formularios para ver los mensajes de estas clases. Los programadores de software de cliente pueden crear nuevas clases de mensaje y formularios personalizados para la visualización de los mensajes creados mediante el uso de las clases nuevas.
  
Cada formulario personalizado implementa un conjunto de comandos del menú estándar, como **Abrir**, **crear**, **Eliminar**y **respuesta**y un conjunto de comandos que son específicos de la forma concreta. Algunos de los comandos de formulario se integran con la interfaz de usuario de la aplicación cliente cuando el formulario está activo; otros comandos de formulario reemplazan completamente los comandos de cliente. 
  
En la siguiente ilustración se muestra la relación entre los componentes MAPI relacionados con el uso de formularios. 
  
**Arquitectura de formulario MAPI**
  
![Arquitectura de formulario MAPI] (media/forms01.gif "Arquitectura de formulario MAPI")
  
En el diagrama, tenga en cuenta que el Administrador de formulario desempeña un papel que es similar a otros proveedores de servicios MAPI, aunque no es un proveedor de servicios de sí mismo. El Administrador de formulario es un archivo DLL reemplazable que implementa algunas de las interfaces MAPI. Aunque los desarrolladores pueden implementar su propio administrador de formularios, mayoría de los entornos utilizará el Administrador de formulario proporcionado por Microsoft debido a la complejidad del director de formulario.
  
En la siguiente lista se describe los componentes en el diagrama y su relación con otros componentes:
  
- Cliente de mensajería: una aplicación que puede usar objetos de formulario. El cliente de mensajería usa las interfaces de formulario MAPI para comunicarse con el Administrador de formulario para cargar los mensajes en los objetos de formulario.
    
- Interfaces de formulario MAPI: un estándar definido para la comunicación entre los componentes MAPI que están relacionadas con los formularios.
    
- Administrador de formularios: el archivo DLL que usan los clientes de mensajería para controlar la instalación de los formularios en las bibliotecas de formularios, la carga de los servidores de formulario y la comunicación inicial entre clientes de mensajería y los servidores de formulario.
    
- Bibliotecas de formularios: ubicación de almacenamiento permanente para los archivos ejecutables asociados con los servidores de formulario.
    
- Servidores de formulario: archivos ejecutables que implementan un formulario. Servidores de formulario crean objetos de formulario e interfaces de usuario para abordar los problemas con mensajes específicos. Este archivo ejecutable también es un servidor OLE y sigue las convenciones usuales de OLE.
    
- Objetos de formulario: objetos de tiempo de ejecución creados por los servidores de formulario que se corresponden con mensajes específicos. Objetos de formulario se ejecuten en el mismo contexto de proceso como su servidor de formulario.
    
Para obtener más información acerca de los componentes de formulario MAPI, vea [Los formularios MAPI](mapi-forms.md).
  
## <a name="see-also"></a>Vea también

- [Arquitectura y las características MAPI](mapi-features-and-architecture.md)

