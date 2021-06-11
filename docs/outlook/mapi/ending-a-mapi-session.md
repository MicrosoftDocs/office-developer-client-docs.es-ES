---
title: Finalización de una sesión MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ca153737-75dc-426a-a410-7a7ab3264f23
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 74c2a7247df02570761247a9e4a6fae378f37312
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287156"
---
# <a name="ending-a-mapi-session"></a>Finalización de una sesión MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes pueden finalizar sus sesiones en respuesta a la solicitud de un usuario, ya sea inmediatamente o después de que se hayan procesado todos los mensajes salientes y cuando se produzca un error crítico. Algunos clientes deben permanecer conectados para que los mensajes salientes pendientes puedan llegar al proveedor de transporte y al sistema de mensajería de destino. Si este cliente envía un mensaje e inmediatamente cierra la sesión, el mensaje puede permanecer en la cola de salida hasta que un usuario vuelva a iniciar sesión y permanezca conectado lo suficiente como para que se transmita el mensaje.
  
 **Cuando necesite finalizar la sesión con el subsistema MAPI**
  
1. Cancele los registros de todas las notificaciones llamando al método **Unadvise** de todos los objetos registrados. 
    
2. Libere todos los objetos abiertos llamando a sus [métodos IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) Los tipos de objetos abiertos pueden incluir receptores de aviso, la tabla de estado, la carpeta Bandeja de salida, uno o más almacenes de mensajes y la libreta de direcciones. 
    
3. Llama [a MAPIFreeBuffer para](mapifreebuffer.md) liberar la memoria de los identificadores de entrada almacenados en caché, como **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
4. Llame a [IMAPISession::Logoff](imapisession-logoff.md), estableciendo la marca MAPI_LOGOFF_UI si permite una interfaz de usuario y la marca MAPI_LOGOFF_SHARED si es propietario de la sesión compartida actual. **El cierre de** sesión notifica a todos los demás clientes que usan la sesión compartida actual que deben cerrar la sesión enviando una notificación de error. 
    
5. Libere el puntero de sesión llamando al método **IUnknown::Release de** la sesión. 
    
6. Si llamó [a OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) durante el inicio de la sesión para inicializar las bibliotecas OLE, desinicializarlas ahora llamando [a OleUninitialize](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx). Solo los clientes que han **llamado a OleInitialize** deben llamar **a OleUninitialize**. 
    
7. Desinicializar las bibliotecas MAPI llamando a [MAPIUninitialize](mapiuninitialize.md). Si llamó a **OleInitialize** en algún momento, asegúrese de que se produzca una llamada a **OleUninitialize** antes de esta llamada a **MAPIUninitialize**. El tiempo es crucial. Si la llamada a **OleUninitialize** se sigue a la llamada a **MAPIUninitialize,** es posible que el cliente termine sin ingratas. 
    
8. Si llamó [a ScInitMapiUtil](scinitmapiutil.md) durante el inicio de la sesión para inicializar la biblioteca de utilidades MAPI, desinicializarla ahora llamando [a DeinitMapiUtil](deinitmapiutil.md). Solo los clientes que han llamado **a ScInitMapiUtil** deben llamar **a DeinitMapiUtil**.
    
> [!NOTE]
> Todos los objetos abiertos deben liberarse antes de la llamada a **IMAPISession::Logoff**. Los objetos que permanecen abiertos después **de llamar a Cerrar** sesión no son válidos; no pueden aceptar llamadas y es posible que nunca se liberan. Si se realiza una llamada a uno de estos objetos, espere que se producirá un error en la llamada. 
  
 MAPI no tiene ningún mecanismo para eliminar dll durante el proceso de cierre de sesión. La DLL de un proveedor de servicios solo se puede eliminar cuando un cliente de configuración, como el Panel de control, llama a su función de punto de entrada de servicio de mensajes con el evento MSG_SERVICE_INSTALL configuración. 
  

