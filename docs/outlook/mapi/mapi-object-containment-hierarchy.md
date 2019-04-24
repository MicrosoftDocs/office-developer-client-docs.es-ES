---
title: Jerarquía de contención de objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 33747835-6eeb-4e07-8f92-3cfa81eecd0f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f5faf3a3d4971b01509d0ff0cfa59451015ba205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345825"
---
# <a name="mapi-object-containment-hierarchy"></a>Jerarquía de contención de objetos MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La relación de contención entre objetos especifica las dependencias que algunos objetos tienen en otros objetos para Access. Para una aplicación cliente, el acceso a objetos concretos permite el acceso a otros usuarios. En algunos casos, la relación de contención entre objetos implementados por un proveedor de servicios sigue una jerarquía lógica. En otros casos, es arbitrario. 
  
Un cliente debe obtener acceso a un objeto de sesión MAPI antes de poder usar muchos otros objetos (por ejemplo, proveedores de servicios y la libreta de direcciones MAPI).
  
La contención del almacén de mensajes se basa en la relación jerárquica entre los objetos del almacén de mensajes: el objeto de almacén de mensajes, las carpetas, los mensajes y los datos adjuntos. Lógicamente, los datos adjuntos se incluyen en mensajes, mensajes en carpetas y carpetas en el almacén de mensajes. La relación de contención coincide con esta jerarquía lógica. Para obtener acceso a un mensaje, por ejemplo, un cliente debe tener primero acceso a la carpeta en la que se encuentra el mensaje. Los objetos de perfiles y estado son ejemplos de una relación de contención más arbitraria. Ambos objetos están disponibles a través de la sesión. 
  
Con algunos objetos, los contenedores proporcionan el único acceso. Los datos adJuntos y los destinatarios son ejemplos de objetos que dependen completamente de sus contenedores. El único acceso a los datos adjuntos o a un destinatario es a través del mensaje al que pertenece. Otros objetos tienen rutas de acceso alternativas. A estos objetos se les asignan identificadores binarios, conocidos como identificadores de entrada, por los proveedores de servicios que los crean. Los identificadores de entrada se pueden usar para obtener acceso a sus objetos directamente, lo que permite a los clientes omitir el árbol de contención. 
  
En la siguiente ilustración se muestra la jerarquía de contención de MAPI. La sesión se encuentra en la parte superior del árbol porque es a través de la sesión que un cliente obtiene acceso a todos los demás objetos. El siguiente nivel incluye la tabla de almacén de mensajes, un objeto Table que enumera las propiedades de todos los proveedores de almacenamiento de mensajes en la sesión actual y la libreta de direcciones para proporcionar acceso a todos los proveedores de la libreta de direcciones. La tabla de almacén de mensajes y la libreta de direcciones se usan para tener acceso a los objetos implementados por proveedores de servicios concretos, que se muestran a continuación, en el orden de contención.
  
**Jerarquía de contención de MAPI**
  
![Jerarquía] de conTención de MAPI (media/amapi_41.gif "Jerarquía") de conTención de MAPI
  
## <a name="see-also"></a>Vea también

- [Introducción a la interfaz y el objeto MAPI](mapi-object-and-interface-overview.md)

