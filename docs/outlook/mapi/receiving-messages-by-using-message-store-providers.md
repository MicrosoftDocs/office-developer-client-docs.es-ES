---
title: Recibir mensajes con proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c93a4b56489c2bfb458e2e1cd872073e64d9998a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418732"
---
# <a name="receiving-messages-by-using-message-store-providers"></a>Recibir mensajes con proveedores de almacenamiento de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de almacenamiento de mensajes no tienen que admitir envíos de mensajes entrantes (es decir, admiten la capacidad de los proveedores de transporte y la cola MAPI para usar el proveedor de almacén de mensajes como punto de entrega para los mensajes). Sin embargo, si su proveedor de almacenamiento de mensajes no admite envíos de mensajes entrantes, no se puede usar como almacén de mensajes predeterminado.
  
Para admitir envíos de mensajes entrantes, su proveedor de almacenamiento de mensajes debe hacer lo siguiente:
  
- Admitir los métodos [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) y [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) para que las aplicaciones cliente puedan encontrar los mensajes entrantes. 
    
- Admitir el método [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) para que la cola MAPI pueda informar al proveedor de almacenamiento de mensajes de que ha recibido un mensaje nuevo. 
    
- Implemente las notificaciones para que los clientes puedan registrarse en la notificación de nuevos mensajes. Las notificaciones son opcionales, pero el proveedor debe implementarlas.
    
La secuencia de llamadas de método que se produce cuando un mensaje entrante se entrega a un almacén de mensajes es la siguiente:
  
1. La cola MAPI llama a [IMsgStore:: OpenEntry](imsgstore-openentry.md) con el [EntryID](entryid.md) de la bandeja de entrada para obtener una interfaz de [IMAPIFolder](imapifolderimapicontainer.md) . 
    
2. La cola MAPI llama a [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) para obtener un nuevo objeto Message. 
    
3. La cola MAPI pasa el objeto de mensaje al proveedor de transporte.
    
4. El proveedor de transporte rellena las propiedades del mensaje con datos del sistema de mensajería subyacente y llama al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) del objeto de mensaje. 
    
5. El proveedor de almacenamiento de mensajes utiliza su método de notificación para informar a los clientes registrados de que ha recibido un nuevo mensaje.
    
6. La cola MAPI llama al método [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) del almacén de mensajes. 
    
## <a name="see-also"></a>Ver también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

