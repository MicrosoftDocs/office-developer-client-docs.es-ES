---
title: Inicializar MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5fde3e7eda8d98eb5080fff360616649b1eb96a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309733"
---
# <a name="initializing-mapi"></a>Inicializar MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Todas las aplicaciones cliente que usan las bibliotecas MAPI deben llamar a la función **MAPIInitialize** . Para obtener más información, vea [MAPIInitialize](mapiinitialize.md). **MAPIInitialize** inicializa datos globales para la sesión y prepara las bibliotecas MAPI para aceptar llamadas. Hay algunos marcadores que es importante establecer en algunas situaciones: 
  
- MAPI_NT_SERVICE
    
    Establezca la marca MAPI_NT_SERVICE si su cliente se implementa como un servicio de Windows. Si el cliente es un servicio de Windows y no establece esta marca, MAPI no la reconocerá como un servicio. 
    
- MAPI_MULTITHREAD_NOTIFICATIONS
    
    La marca MAPI_MULTITHREAD_NOTIFICATIONS está relacionada con el modo en que MAPI administra las notificaciones. MAPI crea una ventana oculta que recibe mensajes de ventana cuando se producen cambios en un objeto que genera notificaciones. Los mensajes de ventana se procesan en algún momento, lo que hace que se envíen las notificaciones y que se llame a los métodos [IMAPIAdviseSink::](imapiadvisesink-onnotify.md) método de Notify apropiados. 
    
- MAPI_NO_COINIT
    
    Establezca la marca MAPI_NO_COINT para que **MAPIInitialize** no intente inicializar com con una llamada a [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx). Si se pasa una estructura **MAPIINIT_0** a **MAPIInitialize** con _ULFLAGS_ establecido en MAPI_NO_COINIT, MAPI asumirá que com ya se ha inicializado y omitirá la llamada a **CoInitialize**.
    
Si no se pasa la marca MAPI_MULTITHREAD_NOTIFICATIONS, MAPI crea la ventana de notificación en el subproceso que se usó para la primera llamada **MAPIInitialize** . MAPI crea la ventana de notificación en un subproceso independiente si se pasa MAPI_MULTITHREAD_NOTIFICATIONS (un subproceso dedicado para controlar las notificaciones). MAPI espera que el subproceso que se usa para crear la ventana de notificación oculta sea el siguiente: 
  
- Tener un bucle de mensajes.
    
- Permanecer desbloqueado durante toda la duración de la sesión.
    
- Tienen una duración mayor que cualquier otro subproceso creado por el cliente. 
    
Puede elegir qué subproceso se usa si se establece una marca en la primera llamada de **MAPIInitialize** . El peligro de permitir que uno de los subprocesos controle las notificaciones es que si el subproceso desaparece, se destruye la ventana de notificación y ya no se pueden enviar notificaciones a ningún otro subproceso. Además, el procesamiento especial puede ser necesario para controlar la distribución de los mensajes de notificación que se publican en la cola de mensajes de la ventana oculta. 
  
Si usa una ventana independiente para controlar las notificaciones, asegúrese de que las notificaciones aparecerán en el momento adecuado en un subproceso adecuado. No necesitará ningún código especial para buscar y procesar los mensajes de Windows que se envían a la ventana de notificación. 
  
MAPI recomienda que los siguientes tipos de aplicaciones cliente usen un subproceso independiente para crear la ventana oculta para la compatibilidad con notificaciones:
  
- Todos los clientes multiproceso.
    
- Servicios de Windows de un solo proceso y aplicaciones de consola Win32.
    
- Clientes de un único subproceso que no necesitan usar su subproceso principal para la notificación.
    
Para usar el enfoque de subprocesos independiente, llame a **MAPIInitialize** en cada subproceso, estableciendo la marca MAPI_MULTITHREAD_NOTIFICATIONS. 
  
> [!NOTE]
> Solo la primera llamada de un cliente a **MAPIInitialize** hace que se cree una ventana oculta para admitir las notificaciones. Las llamadas posteriores solo hacen que se incremente un recuento de referencia. 
  

