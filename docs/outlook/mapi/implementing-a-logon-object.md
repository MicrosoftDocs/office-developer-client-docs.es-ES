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
ms.openlocfilehash: f9d77313012c2d133dc9352707ebc5e0c69c9973
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433048"
---
# <a name="implementing-a-logon-object"></a>Implementar un objeto de inicio de sesión

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cada libreta de direcciones, almacén de mensajes y proveedor de transporte crea una instancia de un objeto de inicio de sesión como parte de su implementación de [IABProvider:: Logon](iabprovider-logon.md), [IMSProvider:: Logon](imsprovider-logon.md)o [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md). Los objetos de inicio de sesión implementan métodos que ayudan a las solicitudes de cliente del servicio MAPI. Según el tipo de proveedor de servicios, el objeto de inicio de sesión será compatible con una de las siguientes interfaces. 
  
|**Interfaz de objeto de inicio de sesión**|**Proveedor de servicios**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |Proveedor de la libreta de direcciones  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |Proveedor de almacenamiento de mensajes  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |Proveedor de transporte  <br/> |
   
La libreta de direcciones y los proveedores de almacenamiento de mensajes implementan las siguientes características en sus objetos de inicio de sesión:
  
- Compatibilidad con la notificación de eventos ( **** métodos Advise y Unadvise).**** Para obtener información general sobre la notificación de eventos, vea [notificación de eventos en MAPI](event-notification-in-mapi.md). Para obtener más información acerca de cómo admitir notificaciones en el objeto de inicio de sesión, consulte [admitir notificación de eventos](supporting-event-notification.md). 
    
- Comparación de identificador de entrada (método**CompareEntryIDs** ). Para obtener información general acerca de los identificadores de entrada, consulte identificadores de [entrada MAPI](mapi-entry-identifiers.md). Para obtener más información acerca de la comparación de identificadores de entrada en el método **CompareEntryIDs** del objeto de inicio de sesión, consulte [support Object Access and](supporting-object-access-and-comparison.md)Comparison.
    
- Acceso a información de error adicional (método**GetLastError** ). Para obtener más información sobre el tratamiento de errores en MAPI, vea [control de errores en MAPI](error-handling-in-mapi.md). 
    
- Acceso a objetos implementados por el proveedor de servicios (método**OpenEntry** ). Para obtener más información, consulte compatibilidad con el [acceso a objetos y la comparación](supporting-object-access-and-comparison.md).
    
- Acceso a un objeto status (método**OpenStatusEntry** ). Para obtener información general acerca de los objetos de estado, consulte [MAPI status Objects](mapi-status-objects.md). Para obtener información específica sobre cómo implementar un objeto status, vea status ( [implementación de objetos](status-object-implementation.md)).
    
- Un proceso de cierre de sesión (método**Logoff** ). Para obtener más información, consulte [apagar un proveedor de servicios](shutting-down-a-service-provider.md).
    
Si su proveedor es un proveedor de la libreta de direcciones, también implementará los siguientes métodos y características asociadas:
  
- [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) para proporcionar una lista de las plantillas que se admiten para crear nuevos destinatarios. Para obtener más información, vea [tablas de uso único](one-off-tables.md) o [implementar una tabla de un proveedor único](implementing-a-provider-one-off-table.md).
    
- [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) para proporcionar acceso a la implementación de un destinatario cuyos datos residen en un proveedor de la libreta de direcciones de host. Para obtener más información, vea [actuar como un proveedor de libreta de direcciones externa](acting-as-a-foreign-address-book-provider.md). 
    
- [IABLogon::P reparerecips](iablogon-preparerecips.md) para asegurarse de que las propiedades adecuadas están disponibles para todos los destinatarios de una lista de destinatarios. Para obtener más información, vea [IABLogon::P reparerecips](iablogon-preparerecips.md). 
    
El objeto de inicio de sesión de un proveedor de transporte, que implementa [IXPLogon: IUnknown](ixplogoniunknown.md), es bastante diferente de los objetos de inicio de sesión implementados por los otros tipos de proveedores de servicios. Tiene solo dos características en común con los demás objetos de inicio de sesión: acceso a un objeto de estado a través del método [IXPLogon:: OpenStatusEntry](ixplogon-openstatusentry.md) y una operación de cierre de sesión mediante el método [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) . Los proveedores de transporte implementan las siguientes características únicas en sus objetos de inicio de sesión: 
  
- Registro para tipos de dirección (método[IXPLogon:: AddressTypes](ixplogon-addresstypes.md) ). Para obtener más información acerca de cómo registrar un tipo de dirección, consulte [proveedor de transporte y modelo operativo de administrador de trabajos en cola MAPI](transport-provider-and-mapi-spooler-operational-model.md).
    
- Control de transmisión de mensajes ([IXPLogon:: StartMessage](ixplogon-startmessage.md), [IXPLogon:: EndMessage](ixplogon-endmessage.md)y métodos [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) ). Para obtener más información, vea [modelo de recepción de mensajes](message-reception-model.md), [interacción con la cola MAPI](interacting-with-the-mapi-spooler.md)y [modelo de envío de mensajes](message-submission-model.md).
    
- Validación de estado interno (método[IXPLogon:: ValidateState](ixplogon-validatestate.md) ). 
    
- Capacidad de descargar o cargar mensajes a petición (método[IXPLogon:: FlushQueues](ixplogon-flushqueues.md) ). Para obtener más información, vea [implementar el método FlushQueues](implementing-the-flushqueues-method.md).
    
- Capacidad para consultar mensajes pendientes ([IXPLogon::P método Oll](ixplogon-poll.md) ). Para obtener más información, vea el [modelo de recepción de mensajes](message-reception-model.md).
    
- Detección del estado de inActividad (método[IXPLogon:: idle](ixplogon-idle.md) ). 
    
- Interacción con el método de administrador de trabajos en cola MAPI ([IXPLogon:: TransportNotify](ixplogon-transportnotify.md) ). 
    
## <a name="see-also"></a>Ver también



[Implementar el inicio de sesión del proveedor de servicios](implementing-service-provider-logon.md)

