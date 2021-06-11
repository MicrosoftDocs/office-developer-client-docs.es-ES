---
title: Información general sobre el administrador de trabajos en cola de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 162957ea17b5a82d4da68340e971d328c85cd9f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432719"
---
# <a name="mapi-spooler-overview"></a>Información general sobre el administrador de trabajos en cola de MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La cola MAPI es una función del proceso de Microsoft Office Outlook que es responsable de enviar mensajes y recibir mensajes desde un sistema de mensajería. La cola MAPI desempeña un papel fundamental en la recepción y entrega de mensajes. Cuando un sistema de mensajería no está disponible, la cola MAPI almacena los mensajes y los reenvía automáticamente más adelante. Esta capacidad de retener o enviar datos cuando sea necesario se conoce como almacenar y reenviar, una característica crítica en entornos donde las conexiones remotas son comunes y el tráfico de red es alto. La cola MAPI se ejecuta como un subproceso en segundo plano dentro de Outlook.
  
La cola MAPI tiene responsabilidades adicionales relacionadas con la distribución de mensajes. Entre estas tareas adicionales se incluyen las siguientes:
  
- Realizar un seguimiento de los tipos de destinatarios que administran proveedores de transporte específicos.
    
- Informar a una aplicación cliente cuando se ha entregado un nuevo mensaje.
    
- Invocar el preprocesamiento y el postprocesamiento de mensajes.
    
- Generación de informes que indican que se ha producido la entrega de mensajes.
    
- Mantener el estado de los destinatarios procesados.
    
En la siguiente ilustración se muestra en un nivel alto cómo fluye un mensaje de un cliente al sistema de mensajería.
  
**Flujo de mensajes salientes**
  
![Flujo de mensajes salientes](media/amapi_46.gif "Flujo de mensajes salientes")
  
El usuario de una aplicación cliente envía un mensaje a uno o varios destinatarios. El proveedor del almacén de mensajes inicia el proceso de envío, formateando el mensaje con información adicional necesaria para la transmisión.
  
La cola MAPI recibe el mensaje para procesar si se produce alguna de las siguientes condiciones:
  
- El proveedor del almacén de mensajes no está estrechamente unido a un proveedor de transporte.
    
- El mensaje requiere preprocesamiento.
    
- El almacén de mensajes y el proveedor de transporte están estrechamente acoplados, pero no pueden controlar todos los destinatarios a los que se dirige el mensaje.
    
Si la cola MAPI recibe el mensaje, realiza cualquier preprocesamiento necesario y entrega el mensaje al proveedor de transporte adecuado. El proveedor de transporte proporciona el mensaje a su sistema de mensajería, que lo envía a su destinatario previsto.
  
Con los mensajes entrantes, el flujo se invierte. El proveedor de transporte recibe un mensaje de su sistema de mensajería y notifica a la cola MAPI. Spooler realiza cualquier postprocesamiento necesario e informa al proveedor del almacén de mensajes de que ha llegado un nuevo mensaje. Esta notificación hace que el cliente actualice su presentación de mensajes, lo que permite al usuario leer el nuevo mensaje.
  
## <a name="see-also"></a>Vea también

- [Características y arquitectura MAPI](mapi-features-and-architecture.md)

