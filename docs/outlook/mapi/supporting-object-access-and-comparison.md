---
title: Compatibilidad con el acceso y la comparación de objetos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2b62f92325fcebf8cd3f0c86d28d98e7ff511ee2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429036"
---
# <a name="supporting-object-access-and-comparison"></a>Compatibilidad con el acceso y la comparación de objetos

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de servicios pueden usar los métodos [IMAPISupport::OpenEntry](imapisupport-openentry.md) e [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) para abrir y comparar objetos que pertenecen a su proveedor o a otros proveedores: 
  
Al igual que [IMAPISession::OpenEntry](imapisession-openentry.md) para clientes, los proveedores pueden usar el método **OpenEntry** de su objeto de soporte técnico para tener acceso a cualquier objeto siempre que conozcan el identificador de entrada del objeto. A diferencia del método session, el método de soporte requiere que especifique un identificador de entrada válido en el _parámetro lpEntryID._ No puede ser NULL. 
  
Para ilustrar cómo un proveedor de transporte puede usar **IMAPISupport::OpenEntry**, tenga en cuenta el siguiente escenario. El proveedor de transporte ha recibido un mensaje con formato de texto enriquecido y no sabe si el destinatario de destino puede controlar este formato. Antes de entregar el mensaje, el proveedor de transporte debe hacer lo siguiente:
  
1. Llame al método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) del mensaje para obtener acceso a la tabla de destinatarios y al identificador de entrada del destinatario, su propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
2. Pase el identificador de entrada a **IMAPISupport::OpenEntry** para abrir el destinatario, normalmente un usuario de mensajería o una lista de distribución. El  _parámetro lpInterface_ debe establecerse en NULL porque el proveedor no puede conocer con antelación el tipo de objeto del destinatario. El método **OpenEntry** del objeto de soporte llama [a IMAPISession::OpenEntry](imapisession-openentry.md) para determinar el proveedor de libreta de direcciones responsable del destinatario. A continuación, el objeto de sesión llama al método **OpenEntry** del proveedor de libreta de direcciones adecuado para abrir el destinatario y devolver un puntero de interfaz al proveedor de transporte. 
    
3. Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) del destinatario para recuperar su **propiedad PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Si **PR_SEND_RICH_INFO** se establece en TRUE, el destinatario puede controlar el texto con formato. 
    
Si ha abierto varios objetos de otros proveedores, es posible que deba averiguar si dos identificadores de entrada hacen referencia al mismo objeto. Por ejemplo, puede tener un identificador de entrada a corto plazo y un identificador de entrada a largo plazo y estos identificadores pueden identificar o no el mismo objeto. Para evitar el procesamiento redundante, llame al [método IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) para comparar estos identificadores de entrada. Debe usar este método para la comparación de identificadores de entrada porque los identificadores de entrada no se pueden comparar directamente. 
  
## <a name="see-also"></a>Vea también



[Proveedores de servicios MAPI](mapi-service-providers.md)

