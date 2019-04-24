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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309586"
---
# <a name="mapi-spooler-overview"></a>Información general sobre el administrador de trabajos en cola de MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La cola MAPI es una función del proceso de Microsoft Office Outlook que se encarga de enviar y recibir mensajes de un sistema de mensajería. La cola MAPI desempeña un papel fundamental en el envío y la entrega de mensajes. Cuando un sistema de mensajería no está disponible, la cola MAPI almacena los mensajes y los reenvía automáticamente en un momento posterior. Esta capacidad de retener datos o enviarlos cuando sea necesario se conoce como almacenamiento y reenvío, una característica crítica en entornos en los que las conexiones remotas son comunes y el tráfico de red es elevado. La cola MAPI se ejecuta como un subproceso en segundo plano en Outlook.
  
La cola MAPI tiene responsabilidades adicionales relacionadas con la distribución de mensajes. Entre estos deberes adicionales se incluyen los siguientes:
  
- Mantener un seguimiento de los tipos de destinatarios que administran los proveedores de transporte específicos.
    
- Informar de una aplicación cliente cuando se ha entregado un nuevo mensaje.
    
- Invocar el preprocesamiento y el procesamiento de mensajes.
    
- Generar informes que indican que se ha producido la entrega de mensajes.
    
- Mantenimiento del estado de los destinatarios procesados.
    
En la siguiente ilustración se muestra a alto nivel cómo fluye un mensaje de un cliente al sistema de mensajería.
  
**Flujo de mensajes salientes**
  
![Flujo de mensajes salientes] (media/amapi_46.gif "Flujo de mensajes salientes")
  
El usuario de una aplicación cliente envía un mensaje a uno o más destinatarios. El proveedor de almacenamiento de mensajes inicia el proceso de envío, da formato al mensaje con la información adicional necesaria para la transmisión.
  
La cola MAPI recibe el mensaje para procesar si se produce alguna de las condiciones siguientes:
  
- El proveedor de almacenamiento de mensajes no está estrechamente acoplado a un proveedor de transporte.
    
- El mensaje requiere preprocesamiento.
    
- El almacén de mensajes y el proveedor de transporte están íntimamente acoplados, pero no pueden administrar todos los destinatarios a los que se dirige el mensaje.
    
Si la cola MAPI recibe el mensaje, realiza los preprocesamientos necesarios y entrega el mensaje al proveedor de transporte correspondiente. El proveedor de transporte entrega el mensaje a su sistema de mensajería, que lo envía a su destinatario previsto.
  
Con los mensajes entrantes, el flujo se invierte. El proveedor de transporte recibe un mensaje de su sistema de mensajería y lo notifica a la cola de impresión de MAPI. La cola de impresión realiza los postprocesamientos necesarios e informa al proveedor del almacén de mensajes que ha recibido un mensaje nuevo. Esta notificación hace que el cliente actualice la presentación del mensaje, lo que permite al usuario leer el nuevo mensaje.
  
## <a name="see-also"></a>Vea también

- [Arquitectura y características de MAPI](mapi-features-and-architecture.md)

