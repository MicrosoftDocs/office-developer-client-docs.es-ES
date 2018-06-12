---
title: Información general sobre la cola de impresión MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 5e4bd4f6038db3dbb33ec3511d953448fea7a6c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818222"
---
# <a name="mapi-spooler-overview"></a>Información general sobre la cola de impresión MAPI
  
**Se aplica a**: Outlook 
  
Cola MAPI es una función del proceso de Microsoft Office Outlook que se encarga de envío de mensajes a y recibir mensajes desde un sistema de mensajería. Cola MAPI desempeña un papel fundamental en la entrega y recepción de mensajes. Cuando un sistema de mensajería no está disponible, cola MAPI almacena los mensajes y los reenvía automáticamente en un momento posterior. Esta capacidad de suspensión en a o enviar datos cuando sea necesario se conoce como almacenar y reenviar, una característica importante en entornos donde las conexiones remotas son comunes y el tráfico de red es alto. Cola MAPI se ejecuta como un subproceso de fondo dentro de Outlook.
  
Cola MAPI tiene responsabilidades adicionales relacionadas con la distribución de mensaje. Estos derechos adicionales son las siguientes:
  
- Seguimiento de los tipos de destinatarios que se controlan mediante proveedores de transporte específica.
    
- Informar a una aplicación cliente cuando se ha entregado un mensaje nuevo.
    
- Mensaje de invocación de preprocesamiento y procesamiento posterior.
    
- Se ha producido la generación de informes que indican que la entrega de mensajes.
    
- Mantenimiento de estado en los destinatarios procesados.
    
En la siguiente ilustración se muestra a un nivel alto, cómo se transmite un mensaje desde un cliente para el sistema de mensajería.
  
**Flujo de mensajes salientes**
  
![Flujo de mensajes de salida] (media/amapi_46.gif "Flujo de mensajes de salida")
  
El usuario de una aplicación cliente envía un mensaje a uno o más destinatarios. El mensaje almacenar proveedor inicia el proceso de envío, dar formato al mensaje con información adicional que sea necesaria para la transmisión.
  
Cola MAPI recibe el mensaje para procesar si se produce alguna de las condiciones siguientes:
  
- El proveedor de almacén de mensajes no se complementa con un proveedor de transporte.
    
- El mensaje requiere preprocesamiento.
    
- El almacén de mensajes y transporte de proveedor se complementa muy bien, pero no pueden administrar todos los destinatarios a quienes está dirigido el mensaje.
    
Si la cola MAPI recibe el mensaje, realiza cualquier preprocesamiento necesarios y entrega el mensaje con el proveedor de transporte apropiado. El proveedor de transporte proporciona el mensaje a su sistema de mensajería, que se envía a su destinatario.
  
Con los mensajes entrantes, se invierte el flujo. El proveedor de transporte recibe un mensaje de su sistema de mensajería y se lo comunica a cola MAPI. Cola de impresión realiza cualquier procesamiento posterior es necesario e informa que el proveedor de almacenamiento de mensaje que ha recibido un nuevo mensaje. Esta notificación hace que el cliente actualizar su presentación de mensajes, permitiendo al usuario leer el mensaje de nuevo.
  
## <a name="see-also"></a>Ver también

- [Arquitectura y las características MAPI](mapi-features-and-architecture.md)

