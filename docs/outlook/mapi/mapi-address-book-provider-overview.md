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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426544"
---
# <a name="mapi-address-book-provider-overview"></a>Introducción al proveedor de libreta de direcciones MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de libreta de direcciones controlan el acceso a la información del directorio. La información de directorio consta de datos para dos tipos de destinatarios de mensajes: usuarios individuales de mensajería y grupos de usuarios de mensajería que se abordan comúnmente juntos en listas de distribución. Según el tipo de destinatario y el proveedor de la libreta de direcciones, hay una amplia variedad de información que se puede hacer disponible. Por ejemplo, todos los proveedores de libretas de direcciones almacenan el nombre, la dirección y el tipo de dirección de un destinatario.
  
Cada proveedor de libreta de direcciones organiza estos datos mediante uno o más contenedores. El número y la estructura de los contenedores depende de la implementación del proveedor de libreta de direcciones. Por ejemplo, un proveedor de libreta de direcciones podría usar un único contenedor para contener toda la información, otro podría usar un contenedor de nivel superior que contiene subcontenedores y un tercero podría usar varios contenedores de nivel superior, cada uno con subcontenedores. Una jerarquía de contenedor de libreta de direcciones puede ser bastante profunda; no hay ningún límite en el número de subcontenedores que se pueden usar.
  
En la siguiente ilustración se muestra una organización típica de libreta de direcciones MAPI.
  
**Organización de la libreta de direcciones**
  
![Organización de libreta de direcciones Organización]de libreta de(media/amapi_04.gif "direcciones")
  
MAPI integra toda la información proporcionada por los proveedores de libreta de direcciones instalados en una única libreta de direcciones, presentando una vista unificada a la aplicación cliente. La lista integrada muestra los contenedores de nivel superior que muestran cada uno de los proveedores de libreta de direcciones instalados. La mayoría de los proveedores de libretas de direcciones exponen solo unos pocos contenedores (normalmente de uno a tres) en el nivel superior para su inclusión en el nivel superior de la libreta de direcciones integrada mapi. Por ejemplo, un proveedor de libreta de direcciones puede hacer disponible "Todos los usuarios" y "Usuarios locales" como dos contenedores en el nivel superior.
  
Los usuarios de aplicaciones cliente pueden ver el contenido de los contenedores de libreta de direcciones y, en algunos casos, modificar el contenido. Los contenedores de libreta de direcciones se pueden crear con diferentes niveles de acceso, según el proveedor de libreta de direcciones. 
  
## <a name="see-also"></a>Vea también

- [Características y arquitectura MAPI](mapi-features-and-architecture.md)

