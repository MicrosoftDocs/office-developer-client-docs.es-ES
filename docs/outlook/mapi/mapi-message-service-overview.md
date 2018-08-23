---
title: Información general sobre el servicio de mensaje MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 58f36a6b-bcc5-4ebb-9761-6f420a718d97
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 56f124d7d42ac41e8b5cdb7cf61c9867bbf69837
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587533"
---
# <a name="mapi-message-service-overview"></a>Información general sobre el servicio de mensaje MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un servicio de mensajes define un grupo de proveedores de servicios relacionados, normalmente los proveedores de servicios que funcionan con el mismo sistema de mensajería. Mientras que los proveedores de servicios de llevar a cabo el trabajo de comunicación entre los sistemas de mensajería y el subsistema MAPI, servicios de mensajes lleve a cabo el trabajo de la interacción entre el usuario y los proveedores de servicios que funcionan con un sistema de mensajería comunes.  
  
Servicios de mensajes existen para facilitar la instalación y configuración de proveedores de servicios para los usuarios. Los usuarios nunca directamente instalan o configuración un proveedor de servicios; el servicio de mensajes completamente administra la instalación y configuración de cada uno de los proveedores de servicios que pertenecen al servicio. Debido a esta característica, los usuarios no necesitan estar familiarizado con los requisitos de configuración del proveedor de servicio específico. 
  
En la siguiente figura se muestra la relación entre una aplicación cliente basada en mensajería y dos servicios de mensaje.
  
**Instalación y configuración de servicio de mensajes**
  
![Configuración e instalación del servicio de mensajes] (media/amapi_44.gif "Configuración e instalación del servicio de mensajes")
  
El usuario invoca el código de instalación de cada servicio de mensajes para agregar el servicio y sus proveedores de servicios a un perfil. En uno de los servicios de mensaje que se muestra en la ilustración, hay tres proveedores de servicios; en el servicio de mensajes, hay dos proveedores de servicios. En algún momento posterior una vez completada, la instalación normalmente en tiempo de inicio de sesión, los proveedores de servicios en cada servicio de mensajes están configurados. El código de configuración de cada servicio de mensajes controla la configuración de los proveedores en el servicio.
  
Cuando se instala un servicio de mensajes, su programa de instalación copia los archivos necesarios desde el origen de instalación en el disco local del usuario y actualiza un archivo de configuración, Mapisvc.inf. El archivo Mapisvc.inf contiene opciones de configuración de todos los servicios de mensajes y proveedores de servicios que se pueden instalar en el equipo. Está organizado en secciones jerárquicas, con vínculos entre cada sección en cada nivel. La sección en el nivel superior contiene información que es relevante para el subsistema MAPI, como una lista de todos los servicios de mensajes disponible y para la instalación de la Ayuda en línea. El siguiente nivel tiene secciones para cada servicio de mensajes, con información como el nombre del archivo DLL del servicio de mensajes y el nombre de su función de punto de entrada de configuración. El tercer nivel tiene secciones con datos de configuración para cada proveedor de servicios en el servicio de mensajes. 
  
Para controlar la configuración, un servicio de mensajes implementa una función de punto de entrada que cumple con un prototipo definido por MAPI y un cuadro de diálogo con fichas conocido como una hoja de propiedades. MAPI llama a la función de punto de entrada para atender las solicitudes de cliente que se relacionan con la administración de perfiles y la administración de proveedores de servicio en el servicio de mensajes. Hojas de propiedades se utilizan para ver y cambiar las propiedades de configuración del proveedor de servicio y de servicio de mensajes. 
  
## <a name="see-also"></a>Recursos adicionales

- [Arquitectura y las características MAPI](mapi-features-and-architecture.md)

