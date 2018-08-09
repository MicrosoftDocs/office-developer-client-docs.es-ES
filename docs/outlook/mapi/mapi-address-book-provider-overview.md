---
title: Introducción al proveedor de la libreta de direcciones MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4bd64aadd5fc18ba79a8717a5c58df72cd3695ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818061"
---
# <a name="mapi-address-book-provider-overview"></a>Introducción al proveedor de la libreta de direcciones MAPI
  
**Hace referencia a**: Outlook 
  
Libreta de direcciones de proveedores de controlar el acceso a información de Active directory. Información de Active Directory se compone de datos para dos tipos de destinatarios del mensaje: individuales de los usuarios y grupos de usuarios de mensajería que con frecuencia se tratan juntos en las listas de distribución de mensajería. Según el tipo de destinatario y el proveedor de la libreta de direcciones, hay una amplia variedad de información que puede estar disponible. Por ejemplo, todos los proveedores de libreta de direcciones almacenan nombre, dirección y tipo de dirección de un destinatario.
  
Cada proveedor de la libreta de direcciones organiza estos datos mediante el uso de uno o varios contenedores. El número y la estructura de los contenedores depende de la implementación del proveedor de la libreta de direcciones. Por ejemplo, un proveedor de libreta de direcciones podría usar un único contenedor para contener toda la información, otro podría usar un contenedor de nivel superior que contiene los subcontenedores y una tercera podría usar varios contenedores de nivel superior, cada subcontenedores de explotación. Una jerarquía de contenedor de la libreta de direcciones puede ser un proceso bastante profunda; No hay ningún límite para el número de subcontenedores que se pueden usar.
  
En la siguiente ilustración muestra una organización típica de la libreta de direcciones MAPI.
  
**Organización de la libreta de direcciones**
  
![Organización de la libreta de direcciones] (media/amapi_04.gif "Organización de la libreta de direcciones")
  
MAPI integra toda la información proporcionada por los proveedores de la libreta de direcciones instalado en una sola libreta de direcciones, presentar una vista unificada a la aplicación cliente. La lista integrada muestra los contenedores de nivel superior que se muestra en cada uno de los proveedores de la libreta de direcciones instalado. La mayoría de los proveedores de la libreta de direcciones exponen solo unos contenedores (normalmente, uno a tres) en el nivel superior para su inclusión en el nivel superior de la libreta de direcciones integrada de MAPI. Por ejemplo, un proveedor de la libreta de direcciones podría realizar disponibles "Todos los usuarios" y "Usuarios locales" como dos contenedores en el nivel superior.
  
Los usuarios de las aplicaciones cliente pueden ver el contenido de los contenedores de la libreta de direcciones y, en algunos casos, modifique el contenido. Contenedores de la libreta de direcciones se pueden crear con distintos niveles de acceso, según el proveedor de la libreta de direcciones. 
  
## <a name="see-also"></a>Vea también

- [Arquitectura y las características MAPI](mapi-features-and-architecture.md)

