---
title: Introducción al servicio de mensajes MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 58f36a6b-bcc5-4ebb-9761-6f420a718d97
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8973cdcee2b10346d0ba07033357b50f7e9a6a27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345986"
---
# <a name="mapi-message-service-overview"></a>Introducción al servicio de mensajes MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un servicio de mensajes define un grupo de proveedores de servicios relacionados, normalmente proveedores de servicios que funcionan con el mismo sistema de mensajería. Mientras que los proveedores de servicios realizan el trabajo de comunicación entre los sistemas de mensajería y el subsistema MAPI, los servicios de mensajes realizan el trabajo de interactuar entre el usuario y los proveedores de servicios que funcionan con un sistema de mensajería común.  
  
Los servicios de mensajería existen para facilitar la instalación y configuración de los proveedores de servicios para los usuarios. Los usuarios nunca instalan o configuran directamente un proveedor de servicios; el servicio de mensajes controla completamente la instalación y la configuración de cada uno de los proveedores de servicios que pertenecen al servicio. Debido a esta característica, los usuarios no necesitan estar familiarizados con los requisitos de configuración de proveedores de servicios específicos. 
  
En la siguiente figura se muestra la relación entre una aplicación cliente basada en mensajería y dos servicios de mensajes.
  
**Instalación y configuración de servicio de mensajes**
  
![Instalación y configuración del servicio de mensajes] (media/amapi_44.gif "Instalación y configuración del servicio de mensajes")
  
El usuario invoca el código de instalación de cada servicio de mensajes para agregar el servicio y sus proveedores de servicios a un perfil. En uno de los servicios de mensajes que se muestran en la figura, hay tres proveedores de servicios; en el otro servicio de mensajes, hay dos proveedores de servicios. En algún momento posterior, una vez completada la instalación, normalmente al iniciar sesión, se configuran los proveedores de servicios de cada servicio de mensajes. El código de configuración de cada servicio de mensajes controla la configuración de los proveedores en el servicio.
  
Cuando se instala un servicio de mensajes, su programa de instalación copia los archivos necesarios del origen de instalación en el disco local del usuario y actualiza un archivo de configuración, MAPISVC. inf. El archivo MAPISVC. inf contiene opciones de configuración para todos los servicios de mensajes y los proveedores de servicios que se pueden instalar en el equipo. Está organizada en secciones jerárquicas, con vínculos entre cada sección de cada nivel. La sección en el nivel superior contiene información relevante para el subsistema MAPI, como una lista de todos los servicios de mensajes disponibles y para la instalación de la ayuda en pantalla. El siguiente nivel tiene secciones para cada servicio de mensajes, con información como el nombre del archivo DLL del servicio de mensajes y el nombre de su función de punto de entrada de configuración. El tercer nivel tiene secciones con datos de configuración para cada proveedor de servicios en el servicio de mensajes. 
  
Para controlar la configuración, un servicio de mensajes implementa una función de punto de entrada que cumple con un prototipo definido por MAPI y un cuadro de diálogo con fichas denominado hoja de propiedades. MAPI llama a la función de punto de entrada para atender las solicitudes de cliente que se relacionan con la administración de perfiles y la administración de proveedores de servicios en el servicio de mensajes. Las hojas de propiedades se usan para ver y cambiar el servicio de mensajes y las propiedades de configuración del proveedor de servicios. 
  
## <a name="see-also"></a>Vea también

- [Arquitectura y características de MAPI](mapi-features-and-architecture.md)

