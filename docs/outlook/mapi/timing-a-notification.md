---
title: Temporización de una notificación
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
# <a name="timing-a-notification"></a>Temporización de una notificación

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Dado que la notificación de eventos es un proceso asincrónico, puede recibir una notificación en cualquier momento, no necesariamente inmediatamente después de que se haya producido el evento.
  
 El tiempo de las llamadas a su [método IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) varía en función del proveedor de servicios que implemente el origen del aviso. Los proveedores de servicios pueden notificar a su cliente: 
  
- Simultáneamente con el evento.
    
- Directamente después del evento.
    
- En algún momento posterior después del evento, posiblemente después de una **llamada Unadvise.** 
    
La mayoría de los proveedores de servicios llaman a **OnNotify** después de que el método MAPI responsable del evento haya devuelto a su autor de la llamada. Por ejemplo, las notificaciones en los mensajes se envían cuando se guardan los cambios realizados en el mensaje, después de la llamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) o cuando se libera el mensaje, después de la llamada **IUnknown::Release.** Hasta que se envía la notificación, no hay cambios visibles en el almacén de mensajes. 
  
Puede recibir notificaciones de un origen de aviso después de haber llamado **a Unadvise** para cancelar un registro. Asegúrese de liberar el receptor de avisos solo después de que su recuento de referencias haya caído a cero, no después de una llamada **de Unadvise correcta.** No suponga que, dado que ha llamado **a Unadvise,** el receptor de avisos ya no es necesario. 
  

