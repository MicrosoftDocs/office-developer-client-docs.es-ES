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
ms.openlocfilehash: 7ff7f79b5e74412e9bbb4b4882c6a7d45e50fe6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420853"
---
# <a name="sending-messages-with-tnef"></a>Enviar mensajes con TNEF

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muchos proveedores de transporte envían automáticamente todos los mensajes salientes con el formato de encapsulación neutro de transporte (TNEF). TNEF se usa para transmitir el texto con formato que muchos clientes y proveedores de almacenes de mensajes admiten en sus mensajes, datos adjuntos de varios tipos y propiedades personalizadas para clases de mensajes personalizadas. Aunque el modo predeterminado para la mayoría de los proveedores de transporte es enviar mensajes salientes con TNEF, algunos proveedores de transporte no lo admiten. La falta de compatibilidad con TNEF no es un problema para los clientes de mensajería estándar que envían y reciben mensajes IPM. Sin embargo, para clientes basados en formularios o clientes que requieren propiedades personalizadas, el uso de TNEF es esencial. Los diseñadores de clientes que dependen de formularios o propiedades personalizadas deben ser conscientes de las capacidades de los proveedores de transporte que usan.
  
Los destinatarios de mensajes pueden controlar si un proveedor de transporte transmite mensajes con TNEF estableciendo la **propiedad PR_SEND_RICH_INFO** transporte. Para obtener más información, **vea PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Cuando la propiedad **PR_SEND_RICH_INFO** de un destinatario se establece en TRUE, un proveedor de transporte que admite TNEF la transmite con el mensaje. Cuando la propiedad se establece en FALSE, se descarta el formato. Cuando **PR_SEND_RICH_INFO** no existe, el proveedor de transporte debe elegir un curso de acción predeterminado. 
  
Cuando los clientes y proveedores de servicios crean un destinatario personalizado, pueden afectar al valor de su propiedad **PR_SEND_RICH_INFO** pasando la marca MAPI_SEND_NO_RICH_INFO en el _parámetro ulFlags_ a la llamada **IAddrBook::CreateOneOff** o **IMAPISupport::CreateOneOff.** Para obtener más información, vea [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) e [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Pasar MAPI_SEND_NO_RICH_INFO hace que MAPI establezca la propiedad PR_SEND_RICH_INFO del destinatario **personalizado** en FALSE; en la mayoría de los casos, no pasar la marca hace que MAPI establezca la propiedad en TRUE. La única excepción es si la dirección del destinatario personalizado se interpreta como una dirección de Internet. En esta situación, MAPI establece **PR_SEND_RICH_INFO** en FALSE. 
  

