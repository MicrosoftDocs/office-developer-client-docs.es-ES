---
title: Finalizar una sesión MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ca153737-75dc-426a-a410-7a7ab3264f23
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e8fa8df4e1439db3f1bc688d282e5ebdd3503024
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575507"
---
# <a name="ending-a-mapi-session"></a>Finalizar una sesión MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes pueden terminar sus sesiones en respuesta a una solicitud de un usuario, ya sea inmediatamente o se han procesado los mensajes salientes después de todo, y cuando se produce un error crítico. Algunos necesitan los clientes para mantenerse iniciar sesión para que los mensajes salientes pendientes puede alcanzar el proveedor de transporte y el sistema de mensajería de destino. Si este tipo de cliente envía un mensaje y se cierra inmediatamente, el mensaje puede permanecer en la cola de salida hasta que un usuario vuelve a iniciar sesión y permanece conectado tiempo suficiente para que el mensaje que se va a transmitir.
  
 **Cuando tenga que terminar la sesión con el subsistema MAPI**
  
1. Cancelar los registros para todas las notificaciones llamando al método **Unadvise** de todos los objetos registrados. 
    
2. Liberar todos los objetos abiertos mediante una llamada a sus métodos [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) . Pueden incluir los tipos de objetos abiertos receptores, la tabla de estado, la carpeta Bandeja de salida, uno o varios almacenes de mensajes y la libreta de direcciones de aviso. 
    
3. Llamar a [MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria para los identificadores de entrada almacenada en caché, como **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
4. Llame a [IMAPISession::Logoff](imapisession-logoff.md), establecer el indicador MAPI_LOGOFF_UI si se permiten una interfaz de usuario y la marca MAPI_LOGOFF_SHARED si es propietario de la sesión compartida actual. **Cierre de sesión** notifica a todos los otros clientes que usan la actual sesión compartida que debe cerrar mediante el envío de una notificación de error. 
    
5. Liberar el puntero de sesión mediante una llamada al método **IUnknown:: Release** de la sesión. 
    
6. Si se llama a [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) durante el inicio de sesión para inicializar las bibliotecas OLE, cancelar la inicialización de ellos ahora llamando [OleUninitialize](http://msdn.microsoft.com/en-us/library/ms691326%28VS.85%29.aspx). Solo los clientes que se han llamado **OleInitialize** deben llamar **OleUninitialize**. 
    
7. Cancelar la inicialización de las bibliotecas de MAPI llamando [MAPIUninitialize](mapiuninitialize.md). Si se llama a **OleInitialize** en algún momento, asegúrese de que una llamada a **OleUninitialize** se produce antes de esta llamada a **MAPIUninitialize**. El momento oportuno es crucial. Si la llamada a **OleUninitialize** sigue a la llamada a **MAPIUninitialize**, su cliente puede terminar incorrectamente. 
    
8. Si se llama a [ScInitMapiUtil](scinitmapiutil.md) durante el inicio de sesión para inicializar la biblioteca de utilidades MAPI, cancelar la inicialización se ahora mediante una llamada a [DeinitMapiUtil](deinitmapiutil.md). Solo los clientes que se han llamado **ScInitMapiUtil** deben llamar a **DeinitMapiUtil**.
    
> [!NOTE]
> Deben liberar todos los objetos abiertos antes de llamar a **IMAPISession::Logoff**. Objetos que permanecen abiertos después de llamar a **cierre de sesión** se convierten en no es válidos; no no aceptan las llamadas y es posible que nunca se liberan. Si se realiza una llamada a uno de estos objetos, esperan que la llamada se lleve a cabo. 
  
 MAPI no tiene ningún mecanismo para eliminar los archivos DLL durante el proceso de cierre de sesión. Un servicio que sólo se puede eliminar archivo DLL del proveedor cuando un cliente de configuración como el Panel de Control llama a su función de punto de entrada del servicio de mensaje con el evento MSG_SERVICE_INSTALL. 
  

