---
title: Enviar mensajes con TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e2df265-b9dd-4e19-8ca5-3e31804e9120
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fb26d854b47894d8f37763b17e5ba0b26fd25ff6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820637"
---
# <a name="sending-messages-with-tnef"></a>Enviar mensajes con TNEF

  
  
**Hace referencia a**: Outlook 
  
Muchos de los proveedores de transporte envían automáticamente todos los mensajes salientes con el formato de encapsulación neutro de transporte (TNEF). TNEF se usa para transmitir el texto con formato que admiten muchos clientes y los proveedores de almacén de mensajes en sus mensajes, datos adjuntos de varios tipos y propiedades personalizadas para las clases de mensaje personalizadas. Aunque es el modo predeterminado para la mayoría de los proveedores de transporte enviar los mensajes salientes con TNEF, algunos proveedores de transporte no lo admiten. La falta de compatibilidad con TNEF no es un problema para los clientes de mensajería estándares que envían y reciben mensajes de IPM. Sin embargo, para los clientes basada en formularios o los clientes que requieren propiedades personalizadas, el uso de TNEF es esencial. Se deben tener en cuenta las capacidades de los proveedores de transporte que utilizan los diseñadores de los clientes que se basan en formularios o propiedades personalizadas.
  
Destinatarios del mensaje pueden controlar o no un proveedor de transporte transmite los mensajes con TNEF estableciendo la propiedad **PR_SEND_RICH_INFO** . Para obtener más información, vea **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Cuando la propiedad **PR_SEND_RICH_INFO** de un destinatario se establece en TRUE, un proveedor de transporte que admite la codificación TNEF transmite con el mensaje. Cuando la propiedad se establece en FALSE, el formato se descarta. Cuando se **PR_SEND_RICH_INFO** no existe, es responsabilidad del proveedor de transporte para elegir una línea predeterminada de acción. 
  
Cuando los clientes y proveedores de servicios crean un destinatario personalizado, pueden afectar al valor de su propiedad **PR_SEND_RICH_INFO** pasando el indicador MAPI_SEND_NO_RICH_INFO en el parámetro _ulFlags_ a la **IAddrBook::CreateOneOff** o ** IMAPISupport::CreateOneOff** de llamadas. Para obtener más información, vea [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) y [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Si se pasa MAPI_SEND_NO_RICH_INFO provoca MAPI establecer la propiedad **PR_SEND_RICH_INFO** del destinatario personalizado en FALSE; en la mayoría de los casos no se pasa el indicador hace que MAPI establecer la propiedad en TRUE. La única excepción es si la dirección del destinatario personalizado se interpreta como una dirección de Internet. En esta uno situación, MAPI establece **PR_SEND_RICH_INFO** en FALSE. 
  

