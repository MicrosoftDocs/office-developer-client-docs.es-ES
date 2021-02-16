---
title: Registro para una notificación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 45625387-dbd2-4ca8-926b-ef87998d01d7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ccc2758b59a9227afbc50360102e793892bbdc52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424906"
---
# <a name="registering-for-a-notification"></a>Registro para una notificación

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un cliente puede registrarse para recibir notificaciones de la libreta de direcciones o del almacén de mensajes como parte de su proceso de inicialización.
  
MAPI admite notificaciones en la libreta de direcciones independientemente de si alguno de los proveedores de libretas de direcciones la admite. La compatibilidad con la notificación en los almacenes de mensajes depende del proveedor de almacenamiento de mensajes en particular. Para determinar si un proveedor de almacenamiento de mensajes determinado admite notificaciones, compruebe su propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Si el almacén de mensajes admite notificaciones, STORE_NOTIFY_OK se establecerá el bit. 
  
Regístrate para recibir notificaciones llamando al método Advise de un **objeto de** origen de aviso. Muchos objetos implementan **Advise** y los clientes pueden registrarse con esos objetos de varias maneras. 
  
 **Para registrar una notificación**
  
1. Cree un objeto receptor de aviso MAPI e incremente su recuento de referencias.
    
2. Si es necesario, llama a [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para crear un objeto receptor de avisos que ajuste el receptor de aviso original y, a continuación, libera el receptor de consejos original. 
    
3. Llama a uno de los siguientes **métodos advise** para completar el registro: 
    
  - Llama [a IMAPISession::Advise](imapisession-advise.md) para registrar notificaciones de sesión o notificaciones en un objeto de libreta de direcciones o almacén de mensajes. 
    
  - Llama a [IAddrBook::Advise](iaddrbook-advise.md) para registrar las notificaciones de la libreta de direcciones o las notificaciones en un usuario de mensajería, un contenedor o una lista de distribución. 
    
  - Llame a [IABLogon::Advise](iablogon-advise.md) para registrarse directamente con un proveedor de libretas de direcciones para recibir notificaciones en un usuario de mensajería, contenedor o lista de distribución. 
    
  - Llama [a IMsgStore::Advise](imsgstore-advise.md) para registrar las notificaciones del almacén de mensajes o las notificaciones de una carpeta o mensaje. 
    
  - Llame a [IMSLogon::Advise](imslogon-advise.md) para registrarse directamente con un proveedor de almacenamiento de mensajes para recibir notificaciones en una carpeta o mensaje. 
    
  - Llame [a IMAPITable::Advise](imapitable-advise.md) para registrar las notificaciones de tabla. 
    
4. Almacenar en caché el número de conexión devuelto de **Advise**.
    
5. Si usa un receptor de aviso ajustado, suéltalo. Una vez registrado el receptor de avisos ajustados, ya no lo necesitará.
    
Calling ** IMAPISession::Advise ** enables you to register for critical error notifications on the overall session or for various notifications on individual objects. Las sesiones envían notificaciones de error crítico a los clientes que han iniciado sesión en sesiones compartidas cuando otro cliente que usa la sesión compartida llama al método [IMAPISession::Logoff.](imapisession-logoff.md) Para registrar las notificaciones de sesión, pase NULL para el parámetro de identificador de entrada. Para registrar notificaciones en un objeto individual, pase el identificador de entrada del objeto. El **método IMAPISession** reenvía la llamada al proveedor de servicios adecuado, según lo determinado por la parte **MAPIUID** del identificador de entrada. Llamar **a IMAPISession::Advise** para registrar notificaciones de objetos es más sencillo que llamar al método Advise de un proveedor **de** servicios. 
  
El registro con la libreta de direcciones es similar a registrarse con la sesión. Para registrar la notificación de error crítico de la libreta de direcciones, pase NULL para el identificador de entrada. Para registrar las notificaciones en un objeto de libreta de direcciones determinado, especifique el identificador de entrada adecuado y el evento o eventos de interés. Tenga en cuenta que muchos proveedores de libretas de direcciones no admiten notificaciones en objetos individuales. En su lugar, admiten notificaciones de tabla en sus tablas de contenido y jerarquía. 
  
Se recomienda liberar el receptor de avisos que implemente o cree con [HrAllocAdviseSink](hrallocadvisesink.md) inmediatamente después de una correcta devolución de una llamada **advise.** Esto se debe a que es posible que los proveedores de servicios liberen el receptor del aviso después de la llamada **de** advise, pero antes de realizar una llamada **Unadvise.** Una vez que haya dado al origen del aviso un puntero al receptor de avisos y el recuento de referencias se haya incrementado en este receptor de avisos, es aconsejable liberarlo a menos que tenga un uso a largo plazo para él. 
  
> [!NOTE]
> Todos los números de conexión que representan registros de aviso válidos no se liberarán hasta que se realiza la llamada **Unadvise.** 
  

