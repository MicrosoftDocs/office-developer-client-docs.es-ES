---
title: Proporcionar informes leídos y no leídos para proveedores de almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 96546d3d766af398ff7acb50f4fc3a479b5668b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432341"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>Proporcionar informes leídos y no leídos para proveedores de almacén de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Si un proveedor de almacén de mensajes puede recibir mensajes, es necesario admitir informes de lectura e informes no leídos de mensajes recibidos por el proveedor del almacén de mensajes. Si un mensaje recibido contiene la propiedad **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) y el valor de esa propiedad es TRUE, el almacén de mensajes debe enviar un mensaje de notificación al remitente cuando el usuario abra el mensaje, lo que indica que el mensaje se ha leído. Del mismo modo, si el usuario elimina el mensaje antes de abrirlo, el almacén de mensajes debe emitir una respuesta al remitente que indique que el mensaje no se leyó.
  
Emitir estos informes es cuestión de crear un objeto [IMessage : IMAPIProp,](imessageimapiprop.md) rellenar las propiedades relevantes del mensaje y enviarlo a la cola MAPI como si el mensaje se hubiera originado con el usuario. Para ello, se puede usar el método [IMAPISupport::ReadReceipt.](imapisupport-readreceipt.md) 
  
> [!NOTE]
> Se debe tener especial cuidado cuando un almacén de mensajes realiza copias de un mensaje no leído con informes pendientes de lectura o no leídos. Estos informes no deben generarse cuando los usuarios leen copias de un mensaje para el que se han solicitado informes. Al realizar una copia de dicho mensaje, el proveedor del almacén de mensajes debe incluir las marcas CLEAR_RN_PENDING y CLEAR_NRN_PENDING en sus llamadas a [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) e [IMessage::SetReadFlag](imessage-setreadflag.md). 
  
## <a name="see-also"></a>Vea también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

