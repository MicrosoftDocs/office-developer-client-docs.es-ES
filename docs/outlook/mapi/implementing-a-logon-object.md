---
title: Implementar un objeto de inicio de sesión
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 99a8473abf01467c534c0ea829e342fa46489e99
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568024"
---
# <a name="implementing-a-logon-object"></a>Implementar un objeto de inicio de sesión

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cada libreta de direcciones, el almacén de mensajes y el proveedor de transporte crea una instancia de un objeto de inicio de sesión como parte de su implementación de [IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)o [IXPProvider::TransportLogon](ixpprovider-transportlogon.md). Objetos de inicio de sesión implementan métodos que ayudan a las solicitudes de cliente de servicio MAPI. Según el tipo de proveedor de servicios, el objeto de inicio de sesión admitirá una de las interfaces siguientes. 
  
|**Interfaz de objeto de inicio de sesión**|**Proveedor de servicios**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |Proveedor de la libreta de direcciones  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |Proveedor de almacén de mensajes  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |Proveedor de transporte  <br/> |
   
Mensaje y la libreta de direcciones almacenan implementan los proveedores las siguientes características en sus objetos de inicio de sesión:
  
- Compatibilidad con la notificación de eventos (métodos**Advise** y **Unadvise** ). Para obtener información general de notificación de eventos, vea [Notificación de evento de MAPI](event-notification-in-mapi.md). Para obtener más información acerca de la compatibilidad de notificación en el objeto de inicio de sesión, vea [Compatibilidad con notificación de evento](supporting-event-notification.md). 
    
- Comparación de identificador de entrada (**CompareEntryIDs** (método)). Para obtener información general acerca de los identificadores de entrada, vea [Identificadores de entrada de MAPI](mapi-entry-identifiers.md). Para obtener más información acerca de la comparación de los identificadores de entrada en **CompareEntryIDs** (método) del objeto de su inicio de sesión, vea [compatibilidad con el acceso a objetos y comparación](supporting-object-access-and-comparison.md).
    
- Acceso a información adicional del error (método**GetLastError** ). Para obtener más información sobre el tratamiento de errores en MAPI, vea [Tratamiento de errores de MAPI](error-handling-in-mapi.md). 
    
- Acceso a objetos de implementada por el proveedor de servicios (método**OpenEntry** ). Para obtener más información, vea [compatibilidad con el acceso a objetos y comparación](supporting-object-access-and-comparison.md).
    
- Acceso a un objeto de estado (método**OpenStatusEntry** ). Para obtener información general acerca de los objetos de estado, vea [Objetos de estado de MAPI](mapi-status-objects.md). Para obtener información específica acerca de cómo implementar un objeto de estado, vea [Implementación de objeto de estado](status-object-implementation.md).
    
- Un proceso de cierre de sesión (método de**cierre de sesión** ). Para obtener más información, vea [Cerrando hacia abajo un proveedor de servicios](shutting-down-a-service-provider.md).
    
Si su proveedor es un proveedor de la libreta de direcciones, además, se implementarán los siguientes métodos y características asociadas:
  
- [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) para proporcionar una lista de las plantillas que admiten para la creación de nuevos destinatarios. Para obtener más información, vea [Las tablas de uso único](one-off-tables.md) o la [implementación de una tabla de uso único proveedor](implementing-a-provider-one-off-table.md).
    
- [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) para proporcionar acceso a la implementación de un destinatario cuyos datos reside en un proveedor de libreta de direcciones de host. Para obtener más información, vea [actuar como un proveedor de libreta de direcciones externa](acting-as-a-foreign-address-book-provider.md). 
    
- [IABLogon::PrepareRecips](iablogon-preparerecips.md) para asegurarse de que las propiedades correspondientes están disponibles para todos los destinatarios en una lista de destinatarios. Para obtener más información, vea [IABLogon::PrepareRecips](iablogon-preparerecips.md). 
    
Objeto de inicio de sesión del proveedor de transporte, que implementa [IXPLogon: IUnknown](ixplogoniunknown.md), es muy diferente de los objetos de inicio de sesión implementados por los otros tipos de proveedores de servicios. Tiene sólo dos características en común con los demás objetos de inicio de sesión: acceso a un objeto de estado a través del método [IXPLogon::OpenStatusEntry](ixplogon-openstatusentry.md) y una operación de cierre de sesión a través del método [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) . Los proveedores de transporte implementan las siguientes características únicas en sus objetos de inicio de sesión: 
  
- En el registro para tipos de direcciones (método[IXPLogon::AddressTypes](ixplogon-addresstypes.md) ). Para obtener más información acerca de cómo registrar un tipo de dirección, vea el [proveedor de transporte y el modelo operacional de cola de impresión de MAPI](transport-provider-and-mapi-spooler-operational-model.md).
    
- Control de transmisión de mensajes (métodos[IXPLogon::StartMessage](ixplogon-startmessage.md), [IXPLogon::EndMessage](ixplogon-endmessage.md)y [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) ). Para obtener más información, vea [Modelo de recepción de mensajes](message-reception-model.md), [interactuar con la cola MAPI](interacting-with-the-mapi-spooler.md)y [Modelo de envío de mensaje](message-submission-model.md).
    
- Validación de estado interno (método[IXPLogon::ValidateState](ixplogon-validatestate.md) ). 
    
- Capacidad para descargar o cargar mensajes a petición (método[IXPLogon::FlushQueues](ixplogon-flushqueues.md) ). Para obtener más información, vea [implementar el método FlushQueues](implementing-the-flushqueues-method.md).
    
- Capacidad para consultar mensajes (método[IXPLogon::Poll](ixplogon-poll.md) ) pendientes. Para obtener más información, vea [Modelo de recepción de mensajes](message-reception-model.md).
    
- Detección de estado inactivo (método[IXPLogon::Idle](ixplogon-idle.md) ). 
    
- Interacción con la cola MAPI (método[IXPLogon::TransportNotify](ixplogon-transportnotify.md) ). 
    
## <a name="see-also"></a>Recursos adicionales



[Implementar el inicio de sesión del proveedor de servicios](implementing-service-provider-logon.md)

