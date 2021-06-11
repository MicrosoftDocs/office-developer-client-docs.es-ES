---
title: Registro de una notificación
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
# <a name="registering-for-a-notification"></a>Registro de una notificación

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un cliente puede registrarse para las notificaciones de la libreta de direcciones o del almacén de mensajes como parte de su proceso de inicialización.
  
MAPI admite notificaciones en la libreta de direcciones independientemente de si alguno de los proveedores de libreta de direcciones la admite. La compatibilidad con notificaciones en almacenes de mensajes depende del proveedor de almacén de mensajes en particular. Para determinar si un proveedor de almacén de mensajes determinado admite notificaciones, compruebe su propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Si el almacén de mensajes admite notificaciones, STORE_NOTIFY_OK se establecerá el bit. 
  
Regístrese para recibir notificaciones llamando al método Advise de un objeto de origen **advise.** Muchos objetos implementan **Advise** y los clientes pueden registrarse con esos objetos de varias maneras. 
  
 **Para registrarse para una notificación**
  
1. Cree un objeto de receptor de aviso MAPI e incremente su recuento de referencias.
    
2. Si procede, llama a [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para crear un objeto de receptor de avisos que envuelva el receptor de aviso original y, a continuación, suelta el receptor de consejos original. 
    
3. Llame a uno de los siguientes **métodos Advise** para completar el registro: 
    
  - Llama [a IMAPISession::Advise](imapisession-advise.md) para registrar las notificaciones de sesión o las notificaciones en un objeto de libreta de direcciones o almacén de mensajes. 
    
  - Llama a [IAddrBook::Advise](iaddrbook-advise.md) para registrarte para notificaciones de libreta de direcciones o para notificaciones en un usuario de mensajería, contenedor o lista de distribución. 
    
  - Llama a [IABLogon::Advise](iablogon-advise.md) para registrarte directamente con un proveedor de libreta de direcciones para recibir notificaciones en un usuario de mensajería, contenedor o lista de distribución. 
    
  - Llama [a IMsgStore::Advise](imsgstore-advise.md) para registrar las notificaciones del almacén de mensajes o las notificaciones en una carpeta o mensaje. 
    
  - Llama a [IMSLogon::Advise](imslogon-advise.md) para registrarte directamente con un proveedor de almacén de mensajes para recibir notificaciones en una carpeta o mensaje. 
    
  - Llama [a IMAPITable::Advise](imapitable-advise.md) para registrarte para las notificaciones de tabla. 
    
4. Almacenar en caché el número de conexión devuelto desde **Advise**.
    
5. Si usa un receptor de aviso ajustado, suéltelo. Una vez registrado el receptor de aviso ajustado, ya no lo necesitará.
    
Llamar a ** IMAPISession::Advise ** permite registrar las notificaciones de errores críticos en la sesión general o para varias notificaciones en objetos individuales. Las sesiones envían notificaciones de error crítico a los clientes que iniciaron sesión compartidas cuando otro cliente que usa la sesión compartida llama al método [IMAPISession::Logoff.](imapisession-logoff.md) Para registrar las notificaciones de sesión, pase NULL para el parámetro de identificador de entrada. Para registrar las notificaciones en un objeto individual, pase el identificador de entrada del objeto. El **método IMAPISession** reenvía la llamada al proveedor de servicios adecuado, según lo determinado por la parte **MAPIUID** del identificador de entrada. Llamar a **IMAPISession::Advise** para registrar las notificaciones de objetos es más sencillo que llamar al método Advise de un proveedor **de** servicios. 
  
El registro con la libreta de direcciones es similar al registro con la sesión. Para registrar la notificación de error crítico de la libreta de direcciones, pase NULL para el identificador de entrada. Para registrar las notificaciones en un objeto de libreta de direcciones determinado, especifique el identificador de entrada adecuado y el evento o eventos de interés. Tenga en cuenta que muchos proveedores de libreta de direcciones no admiten notificaciones en objetos individuales. En su lugar, admiten notificaciones de tabla en sus tablas de jerarquía y contenido. 
  
Es una buena práctica liberar el receptor de avisos que implemente o cree con [HrAllocAdviseSink](hrallocadvisesink.md) inmediatamente después de una devolución correcta de una **llamada advise.** Esto se debe a que es posible que los proveedores de servicios liberen el receptor de avisos después de la llamada **a Advise,** pero antes de realizar una llamada **unadvise.** Una vez que haya dado al origen de aviso un puntero al receptor de avisos y el recuento de referencias se haya incrementado en este receptor de avisos, es aconsejable liberarlo a menos que tenga un uso a largo plazo para él. 
  
> [!NOTE]
> Todos los números de conexión que representan registros de aviso válidos no se liberarán hasta que se realiza la llamada **Unadvise.** 
  

