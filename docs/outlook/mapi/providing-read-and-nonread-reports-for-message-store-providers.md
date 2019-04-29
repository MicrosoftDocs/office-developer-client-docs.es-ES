---
title: Suministro de informes leídos y no leídos para proveedores de almacenamiento de mensajes
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
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>Suministro de informes leídos y no leídos para proveedores de almacenamiento de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Si un proveedor de almacenamiento de mensajes puede recibir mensajes, es necesario que admita informes de lectura y informes no leídos de mensajes recibidos por el proveedor de almacenamiento de mensajes. Si un mensaje recibido contiene la propiedad **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) y el valor de dicha propiedad es true, el almacén de mensajes debería enviar un mensaje de notificación al remitente cuando el usuario abra el mensaje, que indica que se ha leído el mensaje. De forma similar, si el usuario elimina el mensaje antes de abrirlo, el almacén de mensajes debe emitir una respuesta al remitente que indica que no se leyó el mensaje.
  
La emisión de estos informes es una cuestión de crear un objeto [IMessage: IMAPIProp](imessageimapiprop.md) , rellenar las propiedades relevantes del mensaje y enviarlo a la cola de espera de MAPI como si el mensaje se hubiera originado con el usuario. Se puede usar el método [IMAPISupport:: ReadReceipt](imapisupport-readreceipt.md) para esto. 
  
> [!NOTE]
> Debe tener especial cuidado cuando un almacén de mensajes realice copias de un mensaje no leído con informes de lectura o no leídos pendientes. Estos informes no deben generarse cuando los usuarios lean copias de un mensaje para el que se han solicitado informes. Al realizar una copia de este tipo de mensajes, el proveedor de almacenamiento de mensajes debe incluir las marcas CLEAR_RN_PENDING y CLEAR_NRN_PENDING en sus llamadas a [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) y [IMessage:: SetReadFlag](imessage-setreadflag.md). 
  
## <a name="see-also"></a>Ver también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

