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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338496"
---
# <a name="sending-messages-with-tnef"></a>Enviar mensajes con TNEF

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muchos proveedores de transporte envían automáticamente todos los mensajes salientes con el formato de encapsulamiento neutro para el transporte (TNEF). TNEF se usa para transmitir el texto con formato que muchos clientes y proveedores de almacenamiento de mensajes admiten en sus mensajes, datos adjuntos de distintos tipos y propiedades personalizadas para las clases de mensaje personalizadas. Aunque el modo predeterminado para la mayoría de los proveedores de transporte es enviar mensajes salientes con TNEF, algunos proveedores de transporte no lo admiten. La falta de compatibilidad con TNEF no es un problema para los clientes de mensajería estándar que envían y reciben mensajes IPM. Sin embargo, para clientes basados en formularios o clientes que requieran propiedades personalizadas, el uso de TNEF es esencial. Los diseñadores de clientes que se basan en formularios o propiedades personalizadas deben tener en cuenta las capacidades de los proveedores de transporte que usan.
  
Los destinatarios del mensaje pueden controlar si un proveedor de transporte transmite mensajes con TNEF estableciendo la propiedad **PR_SEND_RICH_INFO** . Para obtener más información, vea **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Cuando la propiedad **PR_SEND_RICH_INFO** de un destinatario está establecida en true, un proveedor de transporte que admita TNEF la transmite con el mensaje. Cuando la propiedad se establece en FALSE, se descarta el formato. Cuando **PR_SEND_RICH_INFO** no existe, corresponde al proveedor de transporte elegir un curso de acción predeterminado. 
  
Cuando los clientes y los proveedores de servicios crean un destinatario personalizado, pueden afectar al valor de su propiedad **PR_SEND_RICH_INFO** pasando la marca MAPI_SEND_NO_RICH_INFO en el parámetro _ulFlags_ a **IAddrBook:: CreateOneOff** o ** Llamada a IMAPISupport:: CreateOneOff** . Para obtener más información, vea [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) y [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md). El paso de MAPI_SEND_NO_RICH_INFO hace que MAPI establezca la propiedad **PR_SEND_RICH_INFO** del destinatario personalizado en false; en la mayoría de los casos, no pasar la marca hace que MAPI establezca la propiedad en TRUE. La única excepción es si la dirección del destinatario personalizado se interpreta como una dirección de Internet. En esta única situación, MAPI establece **PR_SEND_RICH_INFO** en false. 
  

