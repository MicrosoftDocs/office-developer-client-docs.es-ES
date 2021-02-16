---
title: Garantizar una notificación Thread-Safe personalizada
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
# <a name="ensuring-a-thread-safe-notification"></a>Garantizar una notificación Thread-Safe personalizada

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Si el cliente se ejecuta en una plataforma multiproceso, es posible que necesite la seguridad de que las llamadas a los métodos [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) se producen en un subproceso determinado. Dado que las llamadas a **OnNotify** suelen producirse en cualquier subproceso, es posible recibir notificaciones en subprocesos inesperados y no deseados, lo que provoca errores que son difíciles de depurar. 
  
Para garantizar que las llamadas a **OnNotify** para una notificación determinada se realizan en el mismo subproceso que se usó para la llamada **advise,** llama a [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) antes de llamar a **Advise**. ** **HrThisThreadAdviseSink**** crea un nuevo objeto receptor de aviso a partir del objeto receptor de avisos. Pase este nuevo objeto en la llamada a **Advise**. Todos los clientes con objetos receptores de aviso que podrían no funcionar fuera del contexto de un subproceso determinado siempre deben registrar los objetos receptores de aviso creados con **HrThisThreadAdviseSink**.
  

