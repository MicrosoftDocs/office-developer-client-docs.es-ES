---
title: Cronometrar una notificación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fa3b155820c64ff55e324c5611eed7348cb93e2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411151"
---
# <a name="timing-a-notification"></a>Cronometrar una notificación

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Dado que la notificación de eventos es un proceso asincrónico, se le puede notificar en cualquier momento, no necesariamente inmediatamente después de que se ha producido el evento.
  
 El tiempo de llamadas al método [IMAPIAdviseSink:: método Notify](imapiadvisesink-onnotify.md) varía en función del proveedor de servicios que implemente el origen de Advise. Los proveedores de servicios pueden notificar al cliente: 
  
- Simultáneamente con el evento.
    
- Justo después del evento.
    
- En un punto posterior después del evento, posiblemente después de una llamada a **Unadvise** . 
    
La mayoría de los proveedores de servicios llaman a **Notify** una vez que el método de MAPI responsable del evento ha vuelto a su autor de la llamada. Por ejemplo, las notificaciones en los mensajes se envían cuando se guardan los cambios en el mensaje después de la llamada a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) o cuando se libera el mensaje, después de la llamada a **IUnknown:: Release** . Hasta que se envíe la notificación, no habrá ningún cambio visible en el almacén de mensajes. 
  
Puede recibir notificaciones de un origen de notificaciones después de haber **** llamado a Unadvise para cancelar un registro. Asegúrese de liberar el receptor de notificaciones solo después de que su recuento de referencia haya caído en cero **** , no después de una llamada de desaconsejar correctamente. No dé por supuesto que, debido a **** que ha llamado a unaconsejar que el receptor de notificaciones ya no es necesario. 
  

