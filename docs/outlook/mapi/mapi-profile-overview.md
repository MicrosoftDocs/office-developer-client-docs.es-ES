---
title: Información general sobre el perfil MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e196800b717ce2528da4b9871bad7425f3a2c326
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385630"
---
# <a name="mapi-profile-overview"></a>Información general sobre el perfil MAPI

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Un perfil es una colección de información acerca de los servicios de mensaje y los proveedores de servicios que un usuario de una aplicación de cliente desea estar disponibles durante una sesión MAPI en particular. Cada usuario tiene al menos un perfil; muchos usuarios mantienen varias. Por ejemplo, un usuario puede tener un perfil para que funcione con un servicio de almacenamiento de mensajes basado en servidor y otro perfil para que funcione con un servicio de almacenamiento de mensajes en el equipo local. Un usuario es posible que desee tener acceso a un conjunto de sistemas de mensajería mediante el uso de los servicios de transporte adecuados para la parte del día y otro conjunto para el resto del día. Los perfiles proporcionan una forma flexible para seleccionar combinaciones de servicios del sistema de mensajería. 
  
Los perfiles pueden tener nombres hasta 64 caracteres alfanuméricos de longitud. Los nombres pueden incluir caracteres de énfasis, el carácter de subrayado y espacios incrustados y no pueden incluir espacios iniciales ni finales. 
  
Los perfiles se organiza jerárquicamente y divididos en secciones, con una sección para cada servicio de mensajes y una sección para cada proveedor de servicios en un servicio. Las secciones relacionadas están vinculadas, haciendo que sea más fácil de navegar por la información. Cada sección contiene una serie de entradas que MAPI o una aplicación cliente que se usa para la configuración.
  
Los movimientos incluidos en un perfil varían de servicio de mensajes al servicio de mensajes. Algunas de las entradas comunes incluyen lo siguiente:
  
- El nombre de cada servicio de mensajes o el proveedor de servicios.
    
- El nombre de los archivos DLL que contienen los proveedores de servicios y los servicios de mensajes.
    
- El nombre de la función de punto de entrada del servicio de cada mensaje.
    
- Una lista de los proveedores de servicios que componen cada servicio de mensajes.
    
Los perfiles se pueden crear en tiempo de instalación, cuando se carga MAPI o un servicio de mensajes en un equipo, o en cualquier momento posterior. MAPI proporciona al Asistente para perfiles de administración de perfiles. 
  
El Asistente para perfiles es una aplicación que crea nuevos perfiles con una cantidad mínima de trabajo. El asistente usa los valores predeterminados para la configuración siempre que sea posible, ahorrando esfuerzo y tiempo a los usuarios. Los usuarios escriben valores sólo cuando sea absolutamente necesario. Para obtener más información, vea [creación de un perfil mediante el Asistente para perfiles](creating-a-profile-by-using-the-profile-wizard.md). También puede usar la herramienta de personalización de Office para crear un nuevo perfil. Para obtener más información, vea [Office Customization Tool](https://go.microsoft.com/fwlink/?LinkId=123000).
  
## <a name="see-also"></a>Vea también



[Arquitectura y las características MAPI](mapi-features-and-architecture.md)

