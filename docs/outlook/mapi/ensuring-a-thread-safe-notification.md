---
title: Garantizar una notificación de seguridad para subProcesos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 88c58d14893f2ac561dc56441eb38b7f4bd0db32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424850"
---
# <a name="ensuring-a-thread-safe-notification"></a>Garantizar una notificación de seguridad para subProcesos

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Si el cliente se ejecuta en una plataforma multiproceso, es posible que necesite garantizar que las llamadas a los métodos [IMAPIAdviseSink:: he Notify](imapiadvisesink-onnotify.md) se producen en un subproceso determinado. Dado que las llamadas a la **Notify** pueden producirse normalmente en cualquier subproceso, es posible recibir notificaciones de subprocesos inesperados y no deseados, lo que provoca errores difíciles de depurar. 
  
Para garantizar que las llamadas a **BENOTIFY** para una notificación concreta se realizan en el mismo subproceso que se usó para la llamada a Advise, llame a [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) antes de llamar a **** Advise. **** * * * * HrThisThreadAdviseSink * * * * crea un nuevo objeto de notificación de notificaciones en el objeto de receptor de notificaciones. Pase este objeto nuevo en la llamada a **Advise**. Todos los clientes con objetos de notificación de notificaciones que podrían no funcionar fuera del contexto de un subproceso concreto deberían registrar siempre los objetos de receptor de avisos creados con **HrThisThreadAdviseSink**.
  

