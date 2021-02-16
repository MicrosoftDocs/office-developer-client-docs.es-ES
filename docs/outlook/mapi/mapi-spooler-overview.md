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
  
La cola MAPI es una función del proceso Microsoft Office Outlook que se encarga de enviar y recibir mensajes de un sistema de mensajería. La cola MAPI desempeña un papel fundamental en la recepción y entrega de mensajes. Cuando un sistema de mensajería no está disponible, la cola MAPI almacena los mensajes y los reenvía automáticamente más adelante. Esta capacidad de retener o enviar datos cuando sea necesario se conoce como almacenar y reenviar, una característica crítica en entornos donde las conexiones remotas son comunes y el tráfico de red es alto. La cola MAPI se ejecuta como un subproceso en segundo plano en Outlook.
  
La cola MAPI tiene responsabilidades adicionales relacionadas con la distribución de mensajes. Entre estas tareas adicionales se incluyen las siguientes:
  
- Realizar un seguimiento de los tipos de destinatarios que administran proveedores de transporte específicos.
    
- Informar a una aplicación cliente cuando se ha entregado un nuevo mensaje.
    
- Invocar preprocesamiento y posprocesamiento de mensajes.
    
- Generación de informes que indican que se ha producido la entrega de mensajes.
    
- Mantener el estado de los destinatarios procesados.
    
En la siguiente ilustración se muestra en un nivel alto cómo fluye un mensaje desde un cliente al sistema de mensajería.
  
**Flujo de mensajes salientes**
  
![Flujo de mensajes salientes Flujo](media/amapi_46.gif "de mensajes salientes")
  
El usuario de una aplicación cliente envía un mensaje a uno o más destinatarios. El proveedor del almacén de mensajes inicia el proceso de envío, formateando el mensaje con información adicional necesaria para la transmisión.
  
La cola MAPI recibe el mensaje para procesar si se produce alguna de las siguientes condiciones:
  
- El proveedor de almacenamiento de mensajes no está estrechamente asociado con un proveedor de transporte.
    
- El mensaje requiere preprocesamiento.
    
- El almacén de mensajes y el proveedor de transporte están estrechamente emparejados, pero no pueden controlar todos los destinatarios a los que se dirige el mensaje.
    
Si la cola MAPI recibe el mensaje, realiza cualquier preprocesamiento necesario y entrega el mensaje al proveedor de transporte adecuado. El proveedor de transporte entrega el mensaje a su sistema de mensajería, que lo envía a su destinatario previsto.
  
Con los mensajes entrantes, el flujo se invierte. El proveedor de transporte recibe un mensaje de su sistema de mensajería y se lo comunica a la cola MAPI. Spooler realiza el posprocesamiento necesario e informa al proveedor de al almacenamiento de mensajes de que ha llegado un nuevo mensaje. Esta notificación hace que el cliente actualice su visualización de mensajes, lo que permite al usuario leer el nuevo mensaje.
  
## <a name="see-also"></a>Consulte también

- [Arquitectura y características mapi](mapi-features-and-architecture.md)

