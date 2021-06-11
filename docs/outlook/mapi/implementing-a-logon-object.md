---
title: Implementación de un objeto Logon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f9d77313012c2d133dc9352707ebc5e0c69c9973
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433048"
---
# <a name="implementing-a-logon-object"></a>Implementación de un objeto Logon

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cada libreta de direcciones, almacén de mensajes y proveedor de transporte crea una instancia de un objeto de inicio de sesión como parte de su implementación de [IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)o [IXPProvider::TransportLogon](ixpprovider-transportlogon.md). Los objetos de inicio de sesión implementan métodos que ayudan a las solicitudes de cliente de servicio MAPI. Según el tipo de proveedor de servicios, el objeto de inicio de sesión admitirá una de las interfaces siguientes. 
  
|**Interfaz de objeto de inicio de sesión**|**Proveedor de servicios**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |Proveedor de libreta de direcciones  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |Proveedor de almacén de mensajes  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |Proveedor de transporte  <br/> |
   
Los proveedores de libreta de direcciones y almacén de mensajes implementan las siguientes características en sus objetos de inicio de sesión:
  
- Compatibilidad con la notificación de eventos **(métodos Advise** y **Unadvise).** Para obtener información general sobre la notificación de eventos, vea [Event Notification in MAPI](event-notification-in-mapi.md). Para obtener más información sobre cómo admitir la notificación en el objeto de inicio de sesión, vea [Supporting Event Notification](supporting-event-notification.md). 
    
- Comparación del identificador de entrada (**método CompareEntryIDs).** Para obtener información general acerca de los identificadores de entrada, vea [Identificadores de entrada MAPI](mapi-entry-identifiers.md). Para obtener más información acerca de la comparación de identificadores de entrada en el método **CompareEntryIDs** del objeto de inicio de sesión, vea [Supporting Object Access and Comparison](supporting-object-access-and-comparison.md).
    
- Acceso a información de error adicional **(método GetLastError).** Para obtener más información sobre cómo controlar errores en MAPI, vea [Control de errores en MAPI](error-handling-in-mapi.md). 
    
- Acceso a objetos implementados por el proveedor de servicios (**método OpenEntry).** Para obtener más información, vea [Supporting Object Access and Comparison](supporting-object-access-and-comparison.md).
    
- Acceso a un objeto status (**método OpenStatusEntry).** Para obtener información general acerca de los objetos de estado, vea [Objetos de estado MAPI](mapi-status-objects.md). Para obtener información específica acerca de la implementación de un objeto de estado, vea [Status Object Implementation](status-object-implementation.md).
    
- Un proceso de cierre de sesión **(método Logoff).** Para obtener más información, vea [Shutting Down a Service Provider](shutting-down-a-service-provider.md).
    
Si su proveedor es un proveedor de libreta de direcciones, también implementará los siguientes métodos y características asociadas:
  
- [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) para proporcionar una lista de las plantillas que admite para crear nuevos destinatarios. Para obtener más información, vea [One-Off Tables](one-off-tables.md) o [Implementing a Provider One-Off Table](implementing-a-provider-one-off-table.md).
    
- [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) para proporcionar acceso a la implementación de un destinatario cuyos datos residen en un proveedor de libreta de direcciones host. Para obtener más información, vea [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md). 
    
- [IABLogon::P repareRecips](iablogon-preparerecips.md) para garantizar que las propiedades adecuadas estén disponibles para todos los destinatarios de una lista de destinatarios. Para obtener más información, vea [IABLogon::P repareRecips](iablogon-preparerecips.md). 
    
El objeto de inicio de sesión de un proveedor de transporte, que implementa [IXPLogon : IUnknown](ixplogoniunknown.md), es bastante diferente de los objetos de inicio de sesión implementados por los otros tipos de proveedores de servicios. Solo tiene dos características en común con los otros objetos de inicio de sesión: acceso a un objeto de estado a través del método [IXPLogon::OpenStatusEntry](ixplogon-openstatusentry.md) y una operación de cierre de sesión a través del método [IXPLogon::TransportLogoff.](ixplogon-transportlogoff.md) Los proveedores de transporte implementan las siguientes características únicas en sus objetos de inicio de sesión: 
  
- Registro para tipos de direcciones ([método IXPLogon::AddressTypes).](ixplogon-addresstypes.md) Para obtener más información acerca del registro de un tipo de dirección, vea [Transport Provider and MAPI Spooler Operational Model](transport-provider-and-mapi-spooler-operational-model.md).
    
- Control de la transmisión de mensajes ([métodos IXPLogon::StartMessage](ixplogon-startmessage.md), [IXPLogon::EndMessage](ixplogon-endmessage.md)y [IXPLogon::SubmitMessage).](ixplogon-submitmessage.md) Para obtener más información, vea [Message Reception Model](message-reception-model.md), [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md)y [Message Submission Model](message-submission-model.md).
    
- Validación de estado interno ([método IXPLogon::ValidateState).](ixplogon-validatestate.md) 
    
- Capacidad para descargar o cargar mensajes a petición ([método IXPLogon::FlushQueues).](ixplogon-flushqueues.md) Para obtener más información, [vea Implementing the FlushQueues Method](implementing-the-flushqueues-method.md).
    
- Capacidad para consultar mensajes pendientes ([método IXPLogon::P oll).](ixplogon-poll.md) Para obtener más información, vea [Message Reception Model](message-reception-model.md).
    
- Detección de estado de inactividad ([método IXPLogon::Idle).](ixplogon-idle.md) 
    
- Interacción con la cola MAPI ([método IXPLogon::TransportNotify).](ixplogon-transportnotify.md) 
    
## <a name="see-also"></a>Vea también



[Implementación del inicio de sesión del proveedor de servicios](implementing-service-provider-logon.md)

