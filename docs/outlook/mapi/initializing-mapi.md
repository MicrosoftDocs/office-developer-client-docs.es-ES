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
ms.openlocfilehash: 5f1dac712731175978bc639cc7296171448a41e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817841"
---
# <a name="initializing-mapi"></a>Inicializar MAPI

  
  
**Hace referencia a**: Outlook 
  
Todas las aplicaciones de cliente que usan las bibliotecas de MAPI deben llamar a la función **MAPIInitialize** . Para obtener más información, vea [MAPIInitialize](mapiinitialize.md). **MAPIInitialize** inicializa datos globales para la sesión y prepara las bibliotecas de MAPI para aceptar llamadas. Hay algunas marcas que son importantes para establecer en algunas situaciones: 
  
- MAPI_NT_SERVICE
    
    Establecer la marca MAPI_NT_SERVICE si su cliente se implementa como un servicio de Windows. Si el cliente es un servicio de Windows y no se establece este marcador, MAPI no la reconocerá como un servicio. 
    
- MAPI_MULTITHREAD_NOTIFICATIONS
    
    El indicador MAPI_MULTITHREAD_NOTIFICATIONS relaciona con cómo MAPI administra las notificaciones. MAPI crea una ventana oculta que recibe los mensajes de ventana cuando se producen cambios a un objeto de generación de notificaciones. Se procesan los mensajes de ventana en algún momento, lo que provoca que las notificaciones se envíen y los métodos de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) apropiados para llamarla. 
    
- MAPI_NO_COINIT
    
    Establecer la marca MAPI_NO_COINT para que no intente inicializar COM con una llamada a [CoInitialize](http://msdn.microsoft.com/en-us/library/ms886303.aspx) **MAPIInitialize** . Si se pasa una estructura **MAPIINIT_0** **MAPIInitialize** con _ulFlags_ establecida en MAPI_NO_COINIT, MAPI asumirá que COM ya se ha inicializado y omitir la llamada a **CoInitialize**.
    
Si no se pasa el indicador MAPI_MULTITHREAD_NOTIFICATIONS, MAPI crea la ventana de notificación en el subproceso que se usó para la primera llamada **MAPIInitialize** . MAPI crea la ventana de notificación en un subproceso independiente, si se pasa MAPI_MULTITHREAD_NOTIFICATIONS: un subproceso dedicado para controlar las notificaciones. MAPI espera del subproceso que se usa para crear la ventana de notificación oculto para: 
  
- Tener un bucle de mensajes.
    
- Permanezca desbloqueada durante la vida útil de la sesión.
    
- Tener una duración mayor que cualquier otro subproceso creado por el cliente. 
    
Puede elegir qué subproceso se usa al establecer una marca en la primera llamada **MAPIInitialize** . El riesgo de que uno de los subprocesos para controlar las notificaciones permite es si desaparece el subproceso, se destruye la ventana de notificación y las notificaciones ya no pueden enviarse a cualquiera de los otros subprocesos. Además, el procesamiento especial podría ser necesarios para controlar el comportamiento de los mensajes de notificación que se registran en la cola de mensajes de la ventana oculta. 
  
Si se utiliza una ventana independiente para controlar las notificaciones, estar seguro de que las notificaciones aparecerá en el momento adecuado en un subproceso adecuado. No necesita ningún código especial para buscar y procesar los mensajes de Windows que están registrados en la ventana de notificación. 
  
MAPI, se recomienda que los siguientes tipos de aplicaciones cliente de utilizan un subproceso independiente para crear la ventana oculta para compatibilidad con notificación:
  
- Todos los clientes de multiproceso.
    
- Aplicaciones de consola de servicios de Windows y Win32 de un único subproceso.
    
- Clientes de un único subproceso que no es necesario usar su subproceso principal para las notificaciones.
    
Para usar el método de subproceso separado, llamar **MAPIInitialize** en cada subproceso, establecer el indicador MAPI_MULTITHREAD_NOTIFICATIONS. 
  
> [!NOTE]
> Sólo un cliente primera llamada a **MAPIInitialize** hace que una ventana oculta que se creará para admitir las notificaciones. Llamadas posteriores causa sólo se incrementa un recuento de referencia. 
  

