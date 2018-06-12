---
title: Una notificación de intervalos de tiempo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 9ee999841b53f358dcee85d4d92c5056f665dbf1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820860"
---
# <a name="timing-a-notification"></a>Una notificación de intervalos de tiempo

  
  
**Se aplica a**: Outlook 
  
Debido a que la notificación de eventos es un proceso asincrónico, puede recibir una notificación en cualquier momento, no necesariamente inmediatamente después de que se ha producido el evento.
  
 La duración de las llamadas al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) varía según el proveedor de servicios de implementar el origen advise. Proveedores de servicios pueden notificar a su cliente, ya sea: 
  
- Simultáneamente con el evento.
    
- Directamente después del evento.
    
- En algún más adelante momento después del evento, posiblemente después de una llamada **Unadvise** . 
    
La mayoría de los proveedores de servicios de llamadas **OnNotify** después de que el método MAPI responsable del evento devuelva a su autor de la llamada. Por ejemplo, en los mensajes se envían cuando se guardan los cambios realizados en el mensaje, después de la llamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , o cuando se libera el mensaje, después de la llamada **IUnknown:: Release** . Hasta que se envía la notificación, no hay ningún cambio está visible en el almacén de mensajes. 
  
Puede recibir notificaciones desde un origen de advise después de haber llamado **Unadvise** para cancelar un registro. Asegúrese de liberar el receptor de notificaciones sólo después de que haya caído su recuento de referencia a cero, no después de una correcta **Unadvise** llamada. No asuma que debido a que se ha llamado **Unadvise** el receptor de notificaciones ya no es necesario. 
  

