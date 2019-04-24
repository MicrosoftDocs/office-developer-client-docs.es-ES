---
title: Introducción al proveedor de servicios MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7cbc79f-3d60-4f21-a378-7b0088ee8ad3
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: bc25158daa9579b5cd6cebe1eee878bf087762a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339973"
---
# <a name="mapi-service-provider-overview"></a>Introducción al proveedor de servicios MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Entre el subsistema MAPI y los sistemas de mensajería son los distintos proveedores de servicios. Los proveedores de servicios son similares a los que conectan las aplicaciones de cliente MAPI a un sistema de mensajería subyacente. Hay tres tipos de proveedores: proveedores de almacenamiento de mensajes, proveedores de directorios o libretas de direcciones, y proveedores de transporte de mensajes. MAPI admite cada tipo de servicio de forma independiente, lo que permite que un proveedor ofrezca uno o varios proveedores de servicios personalizados. Por ejemplo, es posible que un proveedor desee crear un proveedor de libretas de direcciones que use un directorio de libros telefónicos corporativos de empleados o crear un proveedor de almacenamiento de mensajes que use una base de datos existente.
  
Los proveedores de servicios suelen escribirse para sistemas de mensajería específicos por parte de desarrolladores de software que tienen conocimientos o experiencia especializados en un sistema en particular. Por ejemplo, los servicios móviles Microsoft Outlook 2013 y Microsoft Outlook 2010 usan un proveedor de libreta de direcciones para exponer una libreta de direcciones móvil en Outlook. 
  
MAPI presenta a las aplicaciones cliente una vista unificada de la libreta de direcciones y la información del proveedor de transporte. Este enfoque integrado evita que la aplicación cliente tenga que asignar datos al proveedor adecuado. También evita que el usuario tenga que negociar entre varios esquemas de direcciones de la libreta de direcciones y del proveedor de transporte. Sin embargo, la información del proveedor de almacén de mensajes no está unificada y los clientes que usan varios proveedores de almacenamiento de mensajes son los responsables de administrarlas de forma individual.
  
Los proveedores de servicios trabajan con MAPI para crear y enviar mensajes de la siguiente manera: los mensajes se crean usando un formulario que sea adecuado para el tipo o la clase específicos de Message. Muchos mensajes se realizan con el formulario de nota estándar incluido en el subsistema MAPI, ya sea por el usuario de una aplicación cliente o mediante programación sin interacción del usuario. El mensaje completado está dirigido a uno o más destinatarios: un usuario o un grupo de usuarios designados para recibir el mensaje. Un destinatario puede o no tener una entrada en un directorio que posea uno de los proveedores de libreta de direcciones instalados. Los destinatarios que no están asociados con un proveedor de libreta de direcciones instalado se denominan destinatarios personalizados o direcciones de uso único. Una dirección de uso único puede ser temporal y durar hasta que se envíe el mensaje. 
  
Cuando la aplicación cliente envía el mensaje, el proveedor de almacenamiento de mensajes comprueba que cada destinatario tiene una dirección única y válida y que el mensaje tiene toda la información necesaria para la transmisión. Si hay alguna pregunta acerca de un destinatario (por ejemplo, cuando hay varios destinatarios con el mismo nombre), un proveedor de libreta de direcciones se ocupa de resolver la ambigüedad. A continuación, el mensaje se coloca en la cola de salida. 
  
## <a name="see-also"></a>Vea también



[Arquitectura y características de MAPI](mapi-features-and-architecture.md)

