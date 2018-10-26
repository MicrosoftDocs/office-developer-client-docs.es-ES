---
title: Proporcionar notificaciones a proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3722893ae57a108b338725e46c975e92c0f8ff72
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587512"
---
# <a name="providing-notifications-for-message-store-providers"></a>Proporcionar notificaciones a proveedores de almacenamiento de mensajes

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Mientras que las notificaciones son opcionales, son una parte muy importante de un proveedor de almacén de mensaje válida. Las aplicaciones cliente y la cola MAPI se basan en las notificaciones desde el proveedor de almacenamiento de mensajes para obtener un buen rendimiento al enviar los mensajes salientes o recibir mensajes entrantes. Los clientes y la cola MAPI pueden funcionar sin recibir notificaciones desde el proveedor de almacenamiento de mensajes, pero no podrán informar a los usuarios los cambios en el almacén de mensajes sin ellos. Normalmente, esto significa que los usuarios no podrán ver que ha recibido un nuevo mensaje de hasta que su cliente siguiente abre el almacén de mensajes reciben carpeta.
  
Registro de clientes para las notificaciones llamando al método [IMsgStore::Advise](imsgstore-advise.md) . El cliente pasa un [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) de la interfaz, una máscara de bits que indica qué tipo de notificaciones en la que el cliente está interesado en recibir, y un **EntryID** que indica qué objeto en el mensaje de almacenar el **Advise** solicitud se aplica a. Cuando se producen eventos relevantes en el objeto (por ejemplo, cuando llegue un nuevo mensaje en la carpeta de recepción en el almacén de mensajes), el proveedor de almacenamiento de mensaje o el propio objeto debe llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para todas las ** IMAPIAdviseSink** objetos que se hayan registrado para ese tipo de evento. 
  
Incluso si el mensaje almacenar proveedor nunca notifica a otros componentes MAPI de cambios realizados en el almacén de mensajes, aún debe implementar **IMsgStore::Advise** para devolver MAPI_E_NO_SUPPORT. Esto informa a otros componentes para que no espera que el proveedor de almacén de notificaciones desde el mensaje. 
  
## <a name="see-also"></a>Vea también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

