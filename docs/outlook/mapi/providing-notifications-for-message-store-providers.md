---
title: Ofrecer notificaciones para proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a28e6e6f008517a6b1c2c82dfa391b478963880f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328472"
---
# <a name="providing-notifications-for-message-store-providers"></a>Ofrecer notificaciones para proveedores de almacenamiento de mensajes

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Aunque las notificaciones son opcionales, son una parte muy importante de un buen proveedor de almacenamiento de mensajes. Las aplicaciones cliente y la cola MAPI se basan en las notificaciones del proveedor de almacén de mensajes para obtener un buen rendimiento al enviar mensajes salientes o recibir mensajes entrantes. Los clientes y la cola MAPI pueden funcionar sin recibir notificaciones del proveedor de almacén de mensajes, pero no podrán informar a los usuarios de los cambios en el almacén de mensajes sin ellos. Normalmente, esto significa que los usuarios no podrán ver que ha llegado un mensaje nuevo hasta que el cliente Abra la carpeta de recepción del almacén de mensajes.
  
Los clientes se registran para las notificaciones llamando al método [IMsgStore:: Advise](imsgstore-advise.md) . El cliente pasa una interfaz [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) , una máscara de que indica el tipo de notificaciones que el cliente está interesado en recibir y un **EntryID** que indica qué objeto del mensaje almacenará la **notificación** . se aplica la solicitud. Cuando se producen eventos relevantes en el objeto (por ejemplo, cuando llega un nuevo mensaje a la carpeta de recepción en el almacén de mensajes), el proveedor de almacenamiento de mensajes o el propio objeto deben llamar al método [IMAPIAdviseSink:: método Notify](imapiadvisesink-onnotify.md) para todos los ** Objetos IMAPIAdviseSink** que se han registrado para ese tipo de evento. 
  
Incluso si su proveedor de almacenamiento de mensajes nunca notifica a otros componentes MAPI los cambios en el almacén de mensajes, debe implementar **IMsgStore:: Advise** para devolver MAPI_E_NO_SUPPORT. Esto informa a otros componentes de no esperar notificaciones del proveedor del almacén de mensajes. 
  
## <a name="see-also"></a>Vea también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

