---
title: Información general sobre el proveedor de servicio MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7cbc79f-3d60-4f21-a378-7b0088ee8ad3
description: 'Última modificación: 25 de junio de 2012'
ms.openlocfilehash: 14536755c304ede0139b6b1026bb1539a261942f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586413"
---
# <a name="mapi-service-provider-overview"></a>Información general sobre el proveedor de servicio MAPI

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Entre el subsistema MAPI y los sistemas de mensajería son los diversos proveedores de servicios. Proveedores de servicios son similares a los controladores que se conectan las aplicaciones de cliente MAPI a un sistema de mensajería subyacente. Hay tres tipos de proveedores: los proveedores de almacén, la libreta de direcciones o proveedores de Active directory y los proveedores de transporte de mensajes del mensaje. MAPI es compatible con cada tipo de servicio de forma independiente, habilitación de un proveedor que ofrece uno o más proveedores de servicio personalizado. Por ejemplo, es posible que desee un proveedor para crear un proveedor de la libreta de direcciones que usa un directorio corporativo libreta de teléfonos de empleados o para crear un proveedor de almacén de mensajes que usa una base de datos existente.
  
Proveedores de servicios se escriben normalmente para sistemas de mensajería específicos por los programadores de software que tener conocimientos especializados o experimentan con un sistema en particular. Por ejemplo, el Microsoft Outlook 2013 y servicios de Microsoft Outlook 2010 Mobile usan un proveedor de la libreta de direcciones para exponer una libreta de direcciones en Outlook. 
  
MAPI presenta las aplicaciones cliente con una vista unificada de la información del proveedor de transporte y de la libreta de direcciones. Este enfoque integrado impide que la aplicación cliente tener que volver a asignar los datos al proveedor adecuado. También evita que el usuario tenga que negociar entre varios libreta de direcciones y esquemas de direccionamiento de proveedor de transporte. Información del proveedor de almacén de mensajes, sin embargo, no es unificado, y los clientes que usan varios proveedores de almacén de mensajes son responsables de control de forma individual.
  
Los proveedores de servicios funcionan con MAPI para crear y enviar mensajes de la siguiente manera: los mensajes se crean mediante el uso de un formulario que sea apropiado para el tipo específico, o la clase de mensaje. Número de mensajes se realiza con el formulario estándar de nota que se incluye con el subsistema MAPI, ya sea por el usuario de una aplicación cliente o mediante programación sin interacción del usuario. El mensaje finalizado está dirigido a los destinatarios uno o más: un usuario o grupo de usuarios designado para recibir el mensaje. Un destinatario puede o no puede tener una entrada en un directorio que uno de los proveedores de la libreta de direcciones instalado posee. Los destinatarios que no están asociados con un proveedor de la libreta de direcciones instalado se denominan destinatarios personalizados o direcciones de uso único. Una dirección de uso único puede ser temporal, una duración sólo hasta que se envía el mensaje. 
  
Cuando la aplicación cliente envía el mensaje, el proveedor de almacén de mensajes comprueba que cada destinatario tiene una dirección única y válida y que el mensaje tiene toda la información necesaria para la transmisión. Si no hay una pregunta acerca de un destinatario (por ejemplo, cuando hay varios destinatarios con el mismo nombre), un proveedor de la libreta de direcciones se encarga de la resolución de la ambigüedad. A continuación, se sitúa el mensaje en la cola de salida. 
  
## <a name="see-also"></a>Vea también



[Arquitectura y las características MAPI](mapi-features-and-architecture.md)

