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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406258"
---
# <a name="mapi-message-service-overview"></a>Introducción al servicio de mensajes MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un servicio de mensajes define un grupo de proveedores de servicios relacionados, normalmente proveedores de servicios que funcionan con el mismo sistema de mensajería. Mientras que los proveedores de servicios realizan el trabajo de comunicación entre sistemas de mensajería y el subsistema MAPI, los servicios de mensajes realizan el trabajo de interfacing entre el usuario y los proveedores de servicios que trabajan con un sistema de mensajería común.  
  
Los servicios de mensajes existen para facilitar la instalación y configuración de los proveedores de servicios para los usuarios. Los usuarios nunca instalan ni configuran directamente un proveedor de servicios; el servicio de mensajes controla completamente la instalación y configuración de cada uno de los proveedores de servicios que pertenecen al servicio. Debido a esta característica, los usuarios no necesitan estar familiarizados con requisitos de configuración específicos del proveedor de servicios. 
  
En la siguiente figura se muestra la relación entre una aplicación cliente basada en mensajería y dos servicios de mensajes.
  
**Instalación y configuración de servicio de mensajes**
  
![Instalación y configuración del servicio de mensajes]Instalación y configuración del servicio de(media/amapi_44.gif "mensajes")
  
El usuario invoca el código de instalación de cada servicio de mensajes para agregar el servicio y sus proveedores de servicios a un perfil. En uno de los servicios de mensajes que se muestran en la figura, hay tres proveedores de servicios; en el otro servicio de mensajes, hay dos proveedores de servicios. En algún momento posterior después de finalizar la instalación, normalmente en el momento del inicio de sesión, se configuran los proveedores de servicios de cada servicio de mensajes. El código de configuración de cada servicio de mensajes controla la configuración de los proveedores del servicio.
  
Cuando se instala un servicio de mensajes, su programa de instalación copia los archivos necesarios del origen de instalación en el disco local del usuario y actualiza un archivo de configuración, Mapisvc.inf. El archivo Mapisvc.inf contiene opciones de configuración para todos los servicios de mensajes y proveedores de servicios que se pueden instalar en el equipo. Se organiza en secciones jerárquicas, con vínculos entre cada sección en cada nivel. La sección del nivel superior contiene información relevante para el subsistema MAPI, como una lista de todos los servicios de mensajes disponibles y para la instalación de la Ayuda en línea. El siguiente nivel tiene secciones para cada servicio de mensajes, con información como el nombre de archivo DLL del servicio de mensajes y el nombre de su función de punto de entrada de configuración. El tercer nivel tiene secciones con datos de configuración para cada proveedor de servicios del servicio de mensajes. 
  
Para controlar la configuración, un servicio de mensajes implementa una función de punto de entrada que cumple con un prototipo definido por MAPI y un cuadro de diálogo con pestañas conocido como hoja de propiedades. MAPI llama a la función de punto de entrada a las solicitudes de cliente de servicio relacionadas con la administración de perfiles y la administración de proveedores de servicios en el servicio de mensajes. Las hojas de propiedades se usan para ver y cambiar las propiedades de configuración del servicio de mensajes y del proveedor de servicios. 
  
## <a name="see-also"></a>Vea también

- [Características y arquitectura MAPI](mapi-features-and-architecture.md)

