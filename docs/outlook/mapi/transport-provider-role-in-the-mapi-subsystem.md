---
title: Rol de proveedor de transporte en el subsistema MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7659369a-0952-4f5a-a86b-91958c4c1a3f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7ea60b73fb1abe32b6db5e3c73d6ef3fac53d35d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820885"
---
# <a name="transport-provider-role-in-the-mapi-subsystem"></a>Rol de proveedor de transporte en el subsistema MAPI
  
**Hace referencia a**: Outlook 
  
Bibliotecas de vínculos dinámicos del proveedor de transporte (DLL) proporcionan la interfaz entre la cola MAPI y la parte de un sistema de mensajería responsable de enviar y recibir mensajes. La cola MAPI y el proveedor de transporte funcionan conjuntamente para controlar las responsabilidades de enviar un mensaje o recibir un mensaje. La cola MAPI carga el archivo DLL del proveedor de transporte cuando se utiliza en primer lugar y lo libera cuando ya no sea necesaria. Se pueden instalar varios proveedores de transporte en el mismo sistema, pero MAPI proporciona la cola de uno impresión necesario.
  
Las aplicaciones cliente no suele comunicarse directamente con el proveedor de transporte. En su lugar, los clientes de enviar mensajes a través de un proveedor de almacén de y la cola MAPI envía los mensajes salientes para el proveedor de transporte adecuados y entrega los mensajes entrantes en el almacén de mensaje adecuado. La cola MAPI realiza su trabajo y realiza sus llamadas a los proveedores de transporte cuando las aplicaciones de primer plano inactivo. Una vez, opcionalmente, mostrar cuadros de diálogo cuando el proveedor de transporte es el primero iniciado sesión, los proveedores de transporte operan en segundo plano a menos que llame por el cliente para enviar y recibir las colas de vaciado. 
  
Los proveedores de transporte tienen las siguientes responsabilidades en un sistema de mensajería MAPI:
  
- Registre los tipos de direcciones que pueden aceptar con la cola de MAPI para que la cola MAPI puede enviar mensajes al proveedor de transporte adecuados según la dirección de destino de los mensajes. Un proveedor de transporte puede registrar más de un tipo de dirección. Los proveedores de transporte también pueden registrar las direcciones de destinatarios específicos con la cola de MAPI. Los mensajes dirigidos a una de estas direcciones se enviará al proveedor de transporte que se ha registrado la dirección con la cola de MAPI. Para obtener más información, vea [proveedor de transporte y el modelo operacional de cola de impresión de MAPI](transport-provider-and-mapi-spooler-operational-model.md).
    
- Entregar los mensajes entrantes a la cola de MAPI. Dependiendo de la naturaleza del sistema de mensajería, un proveedor de transporte puede ya sea directamente notificar a la cola MAPI cuando llega un nuevo mensaje, o puede solicitar que la cola MAPI sondear al proveedor de transporte periódicamente para comprobar si hay mensajes nuevos.
    
- Convertir las propiedades de mensaje MAPI a y desde las propiedades del mensaje nativas para el sistema de mensajería. Por ejemplo, es posible que el proveedor de transporte debe convertir las direcciones de la dirección del remitente y del destinatario de un mensaje saliente a un formulario que es aceptable para el sistema de mensajería. Algunos sistemas de mensajería no admiten todas las propiedades de mensaje MAPI. Para obtener más información acerca de la conservación de las propiedades de mensaje MAPI para entregar mensajes a un sistema de mensajería, vea [desarrollar un proveedor de transporte TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md).
    
- Registrar el mensaje y el destinatario opciones específicas del proveedor de transporte.
    
- Lleve a cabo cualquier comprobación de credenciales requeridos por el sistema de mensajería.
    
- Acceso a los mensajes salientes mediante el objeto message pasan por la cola de MAPI.
    
- Convertir el formato de mensaje según sea necesario por el sistema de mensajería subyacente.
    
- Notificar a los destinatarios de un mensaje saliente, el proveedor de transporte ha aceptado la responsabilidad de tratamiento estableciendo la propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) para los destinatarios de la cola de MAPI.
    
- Comunicar a la cola MAPI cuando es necesario manipular un mensaje entrante.
    
- Pasar datos del mensaje entrante a la cola MAPI mediante el uso de objetos de mensaje.
    
- Asigne valores a todas las propiedades del mensaje MAPI necesarias en los mensajes entrantes.
    
- Eliminar el mensaje del sistema de mensajería subyacente después de la entrega, si es necesario.
    
- Proporcionar información de estado para las aplicaciones de cliente y de la cola de impresión MAPI.
    
La siguiente ilustración muestra la función del proveedor de transporte con respecto a los demás componentes de la arquitectura MAPI.
  
**Rol de controlador de transporte en un sistema de mensajería**
  
![Rol de proveedor de transporte en un sistema de mensajería] (media/xp01.gif "Rol de proveedor de transporte en un sistema de mensajería")
  

