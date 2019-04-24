---
title: Introducción al proveedor de libreta de direcciones MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ee628f4b11cb174c05a16ca60c9ec830a0e9abbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298148"
---
# <a name="mapi-address-book-provider-overview"></a>Introducción al proveedor de libreta de direcciones MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de la libreta de direcciones administran el acceso a la información del directorio. La información de directorio consta de los datos para dos tipos de destinatarios de mensajes: usuarios de mensajería individuales y grupos de usuarios de mensajería que se suelen tratar juntos en listas de distribución. Según el tipo de destinatario y el proveedor de la libreta de direcciones, existe una amplia variedad de información que puede estar disponible. Por ejemplo, todos los proveedores de la libreta de direcciones almacenan el nombre, la dirección y el tipo de dirección de un destinatario.
  
Cada proveedor de la libreta de direcciones organiza estos datos mediante uno o varios contenedores. El número y la estructura de los contenedores depende de la implementación del proveedor de la libreta de direcciones. Por ejemplo, un proveedor de la libreta de direcciones puede usar un único contenedor para contener toda la información, otro puede usar un contenedor de nivel superior que contenga subcontenedores y un tercero puede usar varios contenedores de nivel superior, cada uno de los cuales contiene subcontenedores. Una jerarquía de contenedores de libretas de direcciones puede ser bastante profunda; no hay ningún límite en el número de subcontenedores que se pueden usar.
  
En la siguiente ilustración se muestra una organización típica de la libreta de direcciones MAPI.
  
**Organización de la libreta de direcciones**
  
![Organización] de la libreta de direcciones (media/amapi_04.gif "Organización") de la libreta de direcciones
  
MAPI integra toda la información proporcionada por los proveedores de libreta de direcciones instalados en una única libreta de direcciones, que presenta una vista unificada de la aplicación cliente. La lista integrada muestra los contenedores de nivel superior que se muestran en cada uno de los proveedores de libreta de direcciones instalados. La mayoría de los proveedores de libreta de direcciones solo exponen unos pocos contenedores (normalmente uno a tres) en el nivel superior para la inclusión en el nivel superior de la libreta de direcciones MAPI integrada. Por ejemplo, un proveedor de libreta de direcciones podría poner a disposición "todos los usuarios" y "usuarios locales" como dos contenedores en el nivel superior.
  
Los usuarios de las aplicaciones cliente pueden ver el contenido de los contenedores de la libreta de direcciones y, en algunos casos, modificar su contenido. Los contenedores de la libreta de direcciones se pueden crear con distintos niveles de acceso, según el proveedor de la libreta de direcciones. 
  
## <a name="see-also"></a>Vea también

- [Arquitectura y características de MAPI](mapi-features-and-architecture.md)

