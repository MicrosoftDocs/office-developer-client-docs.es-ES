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
  
Todas las aplicaciones cliente que usan las bibliotecas MAPI deben llamar a la **función MAPIInitialize.** Para obtener más información, [vea MAPIInitialize](mapiinitialize.md). **MAPIInitialize inicializa** los datos globales de la sesión y prepara las bibliotecas MAPI para aceptar llamadas. Hay algunas marcas que son importantes establecer en algunas situaciones: 
  
- MAPI_NT_SERVICE
    
    Establece la MAPI_NT_SERVICE si el cliente está implementado como un servicio de Windows. Si el cliente es un servicio de Windows y no establece esta marca, MAPI no lo reconocerá como servicio. 
    
- MAPI_MULTITHREAD_NOTIFICATIONS
    
    La MAPI_MULTITHREAD_NOTIFICATIONS se relaciona con la forma en que MAPI administra las notificaciones. MAPI crea una ventana oculta que recibe mensajes de ventana cuando se producen cambios en un objeto que genera notificaciones. Los mensajes de ventana se procesan en algún momento, lo que hace que se envíen las notificaciones y se llame a los métodos [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) adecuados. 
    
- MAPI_NO_COINIT
    
    Establezca la MAPI_NO_COINT para que **MAPIInitialize** no intente inicializar COM con una llamada a [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx). Si se **pasa** una estructura MAPIINIT_0 **a MAPIInitialize** con  _ulFlags_ establecido en MAPI_NO_COINIT, MAPI supondrá que COM ya se ha inicializado y omitirá la llamada a **CoInitialize**.
    
Si MAPI_MULTITHREAD_NOTIFICATIONS marca no se pasa, MAPI crea la ventana de notificación en el subproceso que se usó para la primera **llamada MAPIInitialize.** MAPI crea la ventana de notificación en un subproceso independiente si MAPI_MULTITHREAD_NOTIFICATIONS se pasa, un subproceso dedicado a controlar las notificaciones. MAPI espera que el subproceso que se usa para crear la ventana de notificación oculta haga lo siguiente: 
  
- Tener un bucle de mensaje.
    
- Permanezca desbloqueado durante toda la vida de la sesión.
    
- Tener una duración más larga que cualquier otro subproceso creado por el cliente. 
    
Puede elegir qué subproceso se usa estableciendo una marca en la primera **llamada MAPIInitialize.** El peligro de permitir que uno de tus subprocesos controle las notificaciones es que, si el hilo desaparece, la ventana de notificación se destruye y las notificaciones ya no se pueden enviar a ninguno de tus otros subprocesos. Además, es posible que sea necesario un procesamiento especial para controlar el envío de los mensajes de notificación que se publican en la cola de mensajes de la ventana oculta. 
  
Si usas una ventana independiente para controlar las notificaciones, debes asegurarte de que las notificaciones aparecerán en el momento adecuado en un subproceso adecuado. No necesitará ningún código especial para comprobar y procesar los mensajes de Windows que se publican en la ventana de notificación. 
  
MAPI recomienda que los siguientes tipos de aplicaciones cliente usen un subproceso independiente para crear la ventana oculta para la compatibilidad con notificaciones:
  
- Todos los clientes multiproceso.
    
- Servicios de Windows de subproceso único y aplicaciones de consola win32.
    
- Clientes de subproceso único que no necesitan usar su subproceso principal para la notificación.
    
Para usar el método de subproceso independiente, llame **a MAPIInitialize** en cada subproceso, estableciendo la marca MAPI_MULTITHREAD_NOTIFICATIONS subproceso. 
  
> [!NOTE]
> Solo la primera llamada de un cliente a **MAPIInitialize** hace que se cree una ventana oculta para admitir notificaciones. Las llamadas posteriores solo hacen que se incremente el recuento de referencias. 
  

