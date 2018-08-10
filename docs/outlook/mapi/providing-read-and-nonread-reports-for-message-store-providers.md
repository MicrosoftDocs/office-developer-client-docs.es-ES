---
title: Proporcionar informes de leídos y no leídos a los proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b082d063cc77be46fcd3d4e07ec6753f78f8f335
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820492"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>Proporcionar informes de leídos y no leídos a los proveedores de almacenamiento de mensajes

  
  
**Hace referencia a**: Outlook 
  
Si un proveedor de almacén de mensajes puede recibir los mensajes, es necesario para admitir la lectura de informes e informes de nonread de los mensajes recibidos por el proveedor de almacén de mensajes. Si un mensaje recibido contiene la propiedad **PR_READ_RECEIPT_REQUESTED de MAPI** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) y el valor de la propiedad es TRUE, el almacén de mensajes debe enviar un mensaje de notificación al remitente cuando el usuario abre el mensaje, que indica que se ha leído el mensaje. De forma similar, si el usuario elimina el mensaje antes de abrirlo, el almacén de mensajes debe enviar una respuesta al remitente que indica que no se ha leído el mensaje.
  
Emitir estos informes es una cuestión de creación de un [IMessage: IMAPIProp](imessageimapiprop.md) objeto, rellenar las propiedades relevantes en el mensaje y enviarla a la cola MAPI como si hubiera se originó el mensaje con el usuario. El método [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) se puede usar para esto. 
  
> [!NOTE]
> Debe prestar especial atención cuando un almacén de mensajes realiza copias de un mensaje no leído con pendientes informes de lectura o nonread. No se deben generar dichos informes cuando los usuarios leer todas las copias de un mensaje para el que se han solicitado informes. Al realizar una copia de dicho mensaje, el proveedor de almacenamiento de mensaje debe incluir los indicadores CLEAR_RN_PENDING y CLEAR_NRN_PENDING en sus llamadas a [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) y [IMessage::SetReadFlag](imessage-setreadflag.md). 
  
## <a name="see-also"></a>Vea también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

