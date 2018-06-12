---
title: Soporte de comparación y el acceso a objetos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 2152cfbb91f2e343ebcee3f5b717a29805df1d25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820823"
---
# <a name="supporting-object-access-and-comparison"></a>Soporte de comparación y el acceso a objetos

  
  
**Se aplica a**: Outlook 
  
Proveedores de servicios pueden usar los métodos [IMAPISupport::OpenEntry](imapisupport-openentry.md) y [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) para abrir y comparar los objetos que pertenecen a su proveedor o a otros proveedores: 
  
Como [IMAPISession::OpenEntry](imapisession-openentry.md) para los clientes, proveedores pueden usar el método de **OpenEntry** de sus del objeto de soporte técnico para tener acceso a cualquier objeto como durante cuánto tiempo conozcan identificador de entrada del objeto. A diferencia del método de sesión, el método soporte requiere que se especifique un identificador de entrada válido en el parámetro _lpEntryID_ . No puede ser NULL. 
  
Para ilustrar cómo un proveedor de transporte podría utilizar **IMAPISupport::OpenEntry**, considere el siguiente escenario. El proveedor de transporte ha recibido un mensaje con formato en formato de texto enriquecido y no sabe si el destinatario de destino puede controlar este formato. Antes de entregar el mensaje, el proveedor de transporte debe hacer lo siguiente:
  
1. Llamar al método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) del mensaje para obtener acceso a la tabla de destinatarios y el identificador de entrada del destinatario, su propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
2. Pase el identificador de entrada al **IMAPISupport::OpenEntry** para abrir al destinatario, normalmente, ya sea una lista de distribución o de usuario de mensajería. El parámetro _lpInterface_ debe establecerse en NULL porque el proveedor no conoce de antemano el tipo de objeto del destinatario. El soporte técnico método del objeto **OpenEntry** llama a [IMAPISession::OpenEntry](imapisession-openentry.md) para determinar el proveedor de libreta de direcciones responsable para el destinatario. El objeto de sesión, a continuación, llama al método **OpenEntry** del proveedor de la libreta de dirección adecuada para abrir al destinatario y devolver un puntero de interfaz para el proveedor de transporte. 
    
3. Llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) del destinatario para recuperar su propiedad **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Si **PR_SEND_RICH_INFO** está establecida en TRUE, el destinatario puede controlar el texto con formato. 
    
Si ha abierto varios objetos de otros proveedores, necesitará averiguar si dos identificadores de entrada hacen referencia al mismo objeto. Por ejemplo, es posible que tenga un identificador de entrada a corto plazo y un identificador de entrada a largo plazo y estos identificadores pueden o no se pueden identificar el mismo objeto. Para evitar el procesamiento redundante, llame al método [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) para comparar estos identificadores de entrada. Debe usar este método para la comparación de identificador de entrada debido a que no se pueden comparar directamente los identificadores de entrada. 
  
## <a name="see-also"></a>Ver también



[Proveedores de servicios de MAPI](mapi-service-providers.md)

