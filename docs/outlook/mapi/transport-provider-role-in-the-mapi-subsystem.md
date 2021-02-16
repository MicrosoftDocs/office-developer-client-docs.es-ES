---
title: Rol de proveedor de transporte del subsistema MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7659369a-0952-4f5a-a86b-91958c4c1a3f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7cadb57706e3feec7ed98dd5e4e8d75967036fef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424059"
---
# <a name="transport-provider-role-in-the-mapi-subsystem"></a>Rol de proveedor de transporte del subsistema MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las bibliotecas de vínculos dinámicos (DLL) del proveedor de transporte proporcionan la interfaz entre la cola MAPI y la parte de un sistema de mensajería responsable del envío y recepción de mensajes. La cola MAPI y el proveedor de transporte trabajan conjuntamente para controlar las responsabilidades de enviar un mensaje o recibir un mensaje. La cola MAPI carga la DLL del proveedor de transporte cuando se usa por primera vez y la libera cuando ya no es necesaria. Se pueden instalar varios proveedores de transporte en el mismo sistema, pero MAPI proporciona la cola necesaria.
  
Las aplicaciones cliente normalmente no se comunican directamente con el proveedor de transporte. En su lugar, los clientes envían mensajes a través de un proveedor de almacenamiento y la cola MAPI envía mensajes salientes al proveedor de transporte adecuado y entrega los mensajes entrantes al almacén de mensajes adecuado. La cola MAPI hace su trabajo y realiza sus llamadas a proveedores de transporte cuando las aplicaciones en primer plano están inactivas. Después de mostrar opcionalmente cuadros de diálogo cuando el proveedor de transporte ha iniciado sesión por primera vez, los proveedores de transporte funcionan en segundo plano a menos que el cliente lo llame para vaciar las colas de envío y recepción. 
  
Los proveedores de transporte tienen las siguientes responsabilidades en un sistema de mensajería MAPI:
  
- Registre los tipos de direcciones que pueden aceptar con la cola MAPI para que la cola MAPI pueda enviar mensajes al proveedor de transporte adecuado en función de la dirección de destino de los mensajes. Un proveedor de transporte puede registrar más de un tipo de dirección. Los proveedores de transporte también pueden registrar direcciones de destinatarios específicos con la cola MAPI. Los mensajes dirigidos a una de estas direcciones se envían al proveedor de transporte que registró la dirección con la cola MAPI. Para obtener más información, vea [Proveedor de transporte y Modelo operativo de cola MAPI.](transport-provider-and-mapi-spooler-operational-model.md)
    
- Entregar mensajes entrantes a la cola MAPI. Según la naturaleza del sistema de mensajería, un proveedor de transporte puede notificar directamente a la cola MAPI cuando llega un nuevo mensaje o puede solicitar que la cola MAPI sondee periódicamente al proveedor de transporte para comprobar si hay mensajes nuevos.
    
- Convertir propiedades de mensaje MAPI en y desde propiedades de mensaje nativas en el sistema de mensajería. Por ejemplo, es posible que el proveedor de transporte tenga que convertir las direcciones del remitente y del destinatario en un mensaje saliente en un formulario que sea aceptable para el sistema de mensajería. Algunos sistemas de mensajería no admiten todas las propiedades de los mensajes MAPI. Para obtener más información acerca de cómo conservar las propiedades de los mensajes MAPI al entregar mensajes a un sistema de mensajería, vea Desarrollar un TNEF-Enabled [de transporte de correo](developing-a-tnef-enabled-transport-provider.md)electrónico.
    
- Registre las opciones de mensaje y destinatario específicas del proveedor de transporte.
    
- Realice cualquier comprobación de las credenciales requeridas por el sistema de mensajería.
    
- Obtener acceso a los mensajes salientes mediante el objeto de mensaje pasado por la cola MAPI.
    
- Traducir el formato de mensaje según lo requiera el sistema de mensajería subyacente.
    
- Notifique a la cola MAPI qué destinatarios de un mensaje saliente el proveedor de transporte ha aceptado la responsabilidad de controlar estableciendo la propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) para esos destinatarios.
    
- Informa a la cola MAPI cuando es necesario controlar un mensaje entrante.
    
- Pasar datos de mensajes entrantes a la cola MAPI mediante objetos de mensaje.
    
- Asigne valores a todas las propiedades de mensaje MAPI necesarias en los mensajes entrantes.
    
- Elimine el mensaje del sistema de mensajería subyacente después de la entrega, si es necesario.
    
- Proporcionar información de estado para la cola MAPI y las aplicaciones cliente.
    
En la siguiente ilustración se muestra el rol de un proveedor de transporte con respecto a los demás componentes de la arquitectura MAPI.
  
**Rol de controlador de transporte en un sistema de mensajería**
  
![Rol de proveedor de transporte en un rol de proveedor de]transporte del sistema de mensajería en un sistema de(media/xp01.gif "mensajería")
  

