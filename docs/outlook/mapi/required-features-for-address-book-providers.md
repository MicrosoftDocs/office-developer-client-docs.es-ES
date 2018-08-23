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
ms.openlocfilehash: 919b21490bb3b4418ba291e8e06198028c995b00
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570874"
---
# <a name="required-features-for-address-book-providers"></a>Características necesarias para los proveedores de libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de la libreta de direcciones pueden trabajar con información de los destinatarios que es temporal o permanente, local o remoto, comprensible por uno o varios sistemas de mensajería y con formato para una tabla de base de datos o archivo de disco. Hay una gran variedad de características que puede implementar un proveedor de la libreta de direcciones, con lo que se agregar valor y mejorar la interoperabilidad con los clientes y otros proveedores. Sin embargo, algunas de las características son necesarios.
  
En la siguiente tabla se describe las características que son necesarias de todos los proveedores de libreta de direcciones y los pasos que debe seguir para implementarlos.
  
|**Característica**|**Cómo implementar**|
|:-----|:-----|
|Inicio de sesión  <br/> | Implementar una función de punto de entrada. Para obtener más información, vea [implementar una función de punto de entrada de dirección de la libreta de proveedor](implementing-an-address-book-provider-entry-point-function.md).  <br/>  Implemente el método [IABProvider::Logon](iabprovider-logon.md) . Para obtener más información, vea [implementación de dirección de la libreta de proveedor de inicio de sesión y cierre de sesión](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Cierre de sesión de sesión  <br/> |Implemente el método [IABProvider::Shutdown](iabprovider-shutdown.md) . Para obtener más información, vea [implementación de dirección de la libreta de proveedor de inicio de sesión y cierre de sesión](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Crear los identificadores de entrada  <br/> |Proporcionan soporte para la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Para obtener más información, vea [Identificadores de entrada de MAPI](mapi-entry-identifiers.md) y los [Identificadores de la libreta de direcciones](address-book-identifiers.md).  <br/> |
|Contribuir a la tabla de estado  <br/> | Implementar los métodos apropiados de la [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interfaz. Para obtener más información, vea [Implementación de objeto de estado](status-object-implementation.md).  <br/>  Admite las propiedades de la tabla de estado requerido. Para obtener más información, vea [Las tablas de estado](status-tables.md).  <br/>  Llame a [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md).  <br/> |
|Proporcionar compatibilidad con objeto de estado limitado  <br/> | Implemente el método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) .  <br/>  Devolver MAPI_E_NO_SUPPORT de los otros métodos **IMAPIStatus** .  <br/> |
|Configuración de compatibilidad con interactiva y programática  <br/> | Implementar una función de punto de entrada de servicio de mensaje.  <br/>  Implemente una tabla para mostrar. Para obtener más información, vea [Las tablas para mostrar](display-tables.md) y la [Implementación de tabla para mostrar](display-table-implementation.md).  <br/>  Implementar una hoja de propiedades o llame al método [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) . Para obtener más información, vea [Implementación de la hoja de propiedad](property-sheet-implementation.md).  <br/> |
   
Además, si el proveedor admite la creación de destinatarios, debe proporcionar una lista de plantillas de creación. Proporcionar esta lista implementando el método [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) para incluir todas las plantillas compatibles con su proveedor y el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de cada contenedor para abrir la **PR_CREATE_TEMPLATES** ([ de PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) (propiedad) e incluir todas las plantillas compatibles con el contenedor. Para obtener más información, vea [Implementación de tablas de uso único](implementing-one-off-tables.md).
  

