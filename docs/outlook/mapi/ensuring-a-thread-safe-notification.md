---
title: Asegurar una notificación de seguro para subprocesos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ad10b2ebd835b21f207fd43ecd8aebc7e1f475f4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585307"
---
# <a name="ensuring-a-thread-safe-notification"></a>Asegurar una notificación de seguro para subprocesos

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Si el cliente se ejecuta en una plataforma de multiproceso, puede que tenga la garantía de que las llamadas a los métodos de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) se producen en un subproceso concreto. Debido a que las llamadas a **OnNotify** normalmente pueden suceder en cualquier subproceso, es posible recibir notificaciones en subprocesos inesperados y no deseados, conduce a los errores que son difíciles de depurar. 
  
Para garantizar que las llamadas a **OnNotify** para una notificación en particular se realizan en el mismo subproceso que se usó para la **Advise** llamar, llamar [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) antes de llamar a **Advise**. ** ** HrThisThreadAdviseSink *** crea un nuevo objeto de receptor de advise desde su objeto de receptor advise. Pase el nuevo objeto de la llamada a **Advise**. Todos los clientes con objetos que pueden no funcionar fuera del contexto de un subproceso determinado siempre deben registrar el receptor de notificaciones de aviso objetos del receptor creados con **HrThisThreadAdviseSink**.
  

