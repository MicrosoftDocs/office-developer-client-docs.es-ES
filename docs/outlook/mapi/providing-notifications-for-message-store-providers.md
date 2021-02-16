---
title: Proporcionar notificaciones para proveedores de almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a28e6e6f008517a6b1c2c82dfa391b478963880f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419936"
---
# <a name="providing-notifications-for-message-store-providers"></a>Proporcionar notificaciones para proveedores de almacén de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Aunque las notificaciones son opcionales, son una parte muy importante de un buen proveedor de almacenamiento de mensajes. Las aplicaciones cliente y la cola MAPI dependen de las notificaciones del proveedor del almacén de mensajes para obtener un buen rendimiento al enviar mensajes salientes o recibir mensajes entrantes. Los clientes y la cola MAPI pueden funcionar sin recibir notificaciones del proveedor del almacén de mensajes, pero no podrán informar a los usuarios de los cambios en el almacén de mensajes sin ellos. Normalmente, esto significa que los usuarios no podrán ver que ha llegado un nuevo mensaje hasta que el cliente abra a continuación la carpeta de recepción del almacén de mensajes.
  
Los clientes se registran para recibir notificaciones llamando al [método IMsgStore::Advise.](imsgstore-advise.md) El cliente pasa una interfaz [IMAPIAdviseSink : IUnknown,](imapiadvisesinkiunknown.md) una máscara de bits que indica el tipo de notificaciones que el cliente está interesado en recibir y un **EntryID** que indica a qué objeto del almacén de mensajes se aplica la solicitud **Advise.** Cuando se producen eventos relevantes en el objeto (por ejemplo, cuando llega un nuevo mensaje a la carpeta de recepción del almacén de mensajes), el proveedor del almacén de mensajes o el propio objeto deben llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para todos los objetos **IMAPIAdviseSink** que se han registrado para ese tipo de evento. 
  
Incluso si el proveedor del almacén de mensajes nunca notifica a otros componentes MAPI de los cambios en el almacén de mensajes, aún debe implementar **IMsgStore::Advise** para devolver MAPI_E_NO_SUPPORT. Esto informa a otros componentes de que no deben esperar notificaciones del proveedor del almacén de mensajes. 
  
## <a name="see-also"></a>Consulte también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

