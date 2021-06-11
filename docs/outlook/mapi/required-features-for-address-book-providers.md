---
title: Características necesarias para proveedores de libreta de direcciones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e2ccddd7-65e8-41f6-8e21-a4ae98190a96
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 56ca15440c8d323dbab1b6a92a01941106b86934
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421399"
---
# <a name="required-features-for-address-book-providers"></a>Características necesarias para proveedores de libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de libreta de direcciones pueden trabajar con información de destinatarios temporal o permanente, local o remota, comprensible por uno o varios sistemas de mensajería y con formato para un archivo de disco o una tabla de base de datos. Hay una variedad de características que un proveedor de libreta de direcciones puede implementar, lo que agrega valor y mejora la interoperabilidad con clientes y otros proveedores. Sin embargo, se requieren algunas características.
  
En la tabla siguiente se describen las características necesarias para todos los proveedores de libretas de direcciones y los pasos que debe seguir para implementarlas.
  
|**Característica**|**Cómo se debe implementar**|
|:-----|:-----|
|Inicio de sesión  <br/> | Implementar una función de punto de entrada. Para obtener más información, vea [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).  <br/>  Implemente el [método IABProvider::Logon.](iabprovider-logon.md) Para obtener más información, vea [Implementing Address Book Provider Logon and Logoff](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Cierre de sesión  <br/> |Implemente [el método IABProvider::Shutdown.](iabprovider-shutdown.md) Para obtener más información, vea [Implementing Address Book Provider Logon and Logoff](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Crear identificadores de entrada  <br/> |Proporcione compatibilidad con la **propiedad PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Para obtener más información, vea [Identificadores de entrada MAPI](mapi-entry-identifiers.md) e [Identificadores de libreta de direcciones](address-book-identifiers.md).  <br/> |
|Contribuir a la tabla de estado  <br/> | Implemente los métodos adecuados de la [interfaz IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) Para obtener más información, vea [Status Object Implementation](status-object-implementation.md).  <br/>  Admite las propiedades de tabla de estado necesarias. Para obtener más información, vea [Tablas de estado](status-tables.md).  <br/>  Llame [a IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md).  <br/> |
|Proporcionar compatibilidad con objetos de estado limitado  <br/> | Implemente [el método IMAPIStatus::ValidateState.](imapistatus-validatestate.md)  <br/>  Devuelve MAPI_E_NO_SUPPORT de los otros **métodos IMAPIStatus.**  <br/> |
|Compatibilidad con la configuración interactiva y programática  <br/> | Implementar una función de punto de entrada de servicio de mensajes.  <br/>  Implementar una tabla para mostrar. Para obtener más información, vea [Mostrar tablas](display-tables.md) e implementación de tablas [para mostrar.](display-table-implementation.md)  <br/>  Implemente una hoja de propiedades o llame al [método IMAPISupport::D oConfigPropsheet.](imapisupport-doconfigpropsheet.md) Para obtener más información, vea [Property Sheet Implementation](property-sheet-implementation.md).  <br/> |
   
Además, si el proveedor admite la creación de destinatarios, debe proporcionar una lista de plantillas de creación. Proporcione esta lista implementando el método [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) para incluir todas las plantillas admitidas por el proveedor y el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de cada contenedor para abrir la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) e incluir todas las plantillas admitidas por el contenedor. Para obtener más información, vea [Implementing One-Off Tables](implementing-one-off-tables.md).
  

