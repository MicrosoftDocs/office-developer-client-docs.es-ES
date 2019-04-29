---
title: Características necesarias para los proveedores de libreta de direcciones
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
# <a name="required-features-for-address-book-providers"></a>Características necesarias para los proveedores de libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de libretas de direcciones pueden trabajar con información de destinatarios que sea temporal o permanente, local o remota, comprensible para uno o varios sistemas de mensajería y que tengan el formato de un archivo de disco o una tabla de base de datos. Hay una variedad de características que puede implementar un proveedor de libreta de direcciones, lo que aumenta el valor y mejora la interoperabilidad con clientes y otros proveedores. Sin embargo, se necesitan algunas características.
  
En la tabla siguiente se describen las características necesarias de todos los proveedores de la libreta de direcciones y los pasos que debe seguir para implementarlos.
  
|**Característica**|**Cómo implementar**|
|:-----|:-----|
|Inicio de sesión  <br/> | Implemente una función de punto de entrada. Para obtener más información, vea [implementar una función de punto de entrada de proveedor de libreta de direcciones](implementing-an-address-book-provider-entry-point-function.md).  <br/>  Implemente el método [IABProvider:: Logon](iabprovider-logon.md) . Para obtener más información, vea [implementar el inicio y cierre de sesión del proveedor de libreta de direcciones](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Cierre de sesión  <br/> |Implemente el método [IABProvider:: Shutdown](iabprovider-shutdown.md) . Para obtener más información, vea [implementar el inicio y cierre de sesión del proveedor de libreta de direcciones](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Crear identificadores de entrada  <br/> |Proporcionar compatibilidad con la **** propiedad de ([PidTagEntryId](pidtagentryid-canonical-property.md)). Para obtener más información, consulte identificadores de [entrada MAPI](mapi-entry-identifiers.md) e identificadores de la [Libreta de direcciones](address-book-identifiers.md).  <br/> |
|Contribuir a la tabla de estado  <br/> | Implemente los métodos apropiados de la interfaz [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) . Para obtener más información, vea [implementación de objetos de estado](status-object-implementation.md).  <br/>  Admitir las propiedades de tabla de estado necesarias. Para obtener más información, vea [tablas de estado](status-tables.md).  <br/>  Llamar a [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md).  <br/> |
|Proporcionar compatibilidad con objetos de estado limitados  <br/> | Implemente el método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) .  <br/>  Devuelve MAPI_E_NO_SUPPORT de los otros métodos **IMAPIStatus** .  <br/> |
|Compatibilidad con la configuración interactiva y mediante programación  <br/> | Implemente una función de punto de entrada del servicio de mensajes.  <br/>  Implemente una tabla de presentación. Para obtener más información, consulte [Display](display-tables.md) tables and [Display Table Implementation](display-table-implementation.md).  <br/>  Implemente una hoja de propiedades o llame al método [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) . Para obtener más información, vea implementación de la [hoja de propiedades](property-sheet-implementation.md).  <br/> |
   
Además, si el proveedor admite la creación de destinatarios, debe proporcionar una lista de plantillas de creación. Proporcione esta lista mediante la implementación del método [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) para incluir todas las plantillas admitidas por el proveedor y el método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) de cada contenedor para abrir el **PR_CREATE_TEMPLATES** ([ PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) e incluya todas las plantillas admitidas por el contenedor. Para obtener más información, vea [implementar tablas de un solo uso](implementing-one-off-tables.md).
  

