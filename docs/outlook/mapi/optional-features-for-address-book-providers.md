---
title: Características opcionales para proveedores de libretas de direcciones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1558259-7f0b-4731-80d2-88e51e203df0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9f5d8f0cd1b21f58e4e5c7d7ccd6cb19f3626c38
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414574"
---
# <a name="optional-features-for-address-book-providers"></a>Características opcionales para proveedores de libretas de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Existen muchas características opcionales para los proveedores de libretas de direcciones. Algunas de las características más implementadas incluyen:
  
- Actuar como un proveedor externo al permitir que las entradas de uno de los contenedores se agregarán al contenedor de otro proveedor.
    
- Actuar como proveedor de host agregando entradas de otro proveedor a uno de los contenedores.
    
- Búsqueda avanzada.
    
- Prefijo que se desplaza por las tablas de contenido.
    
- Compatibilidad con listas de distribución.
    
- Compatibilidad con la notificación de eventos.
    
En la tabla siguiente se describen brevemente estas características opcionales y cómo implementarlas:
  
|**Característica**|**Cómo implementar**|
|:-----|:-----|
|Plantillas de suministro para crear entradas para listas de destinatarios de mensajes  <br/> |Implemente [el método IABLogon::GetOneOffTable.](iablogon-getoneofftable.md) Para obtener más información, vea [Tablas de uso único](one-off-tables.md) e implementación One-Off [tablas.](implementing-one-off-tables.md)  <br/> |
|Agrupar destinatarios en una unidad con nombre  <br/> |Admite las propiedades de las listas de distribución mediante la implementación de [la interfaz IDistList : IMAPIContainer.](idistlistimapicontainer.md)  <br/> |
|Actuar como proveedor externo de libretas de direcciones al permitir que las entradas se puedan agregar a un contenedor en otro proveedor  <br/> | Admite el enlace de código a datos en el proveedor de host mediante:  <br/>  Compatibilidad con la **propiedad PR_TEMPLATEID** ([PidTagTemplateid)](pidtagtemplateid-canonical-property.md)en los usuarios de mensajería y las listas de distribución. Para obtener más información, vea [Identificadores de libreta de direcciones.](address-book-identifiers.md)  <br/>  Implementar el [método IABLogon::OpenTemplateID.](iablogon-opentemplateid.md) Para obtener más información, vea [Actuar como proveedor externo de libreta de direcciones.](acting-as-a-foreign-address-book-provider.md)  <br/> |
|Actuar como proveedor de libretas de direcciones host insertando entradas de otro proveedor  <br/> |Admite el enlace de datos a código de un proveedor externo mediante una llamada al método [IMAPISupport::OpenTemplateID.](imapisupport-opentemplateid.md) Para obtener más información, vea [Actuar como proveedor de libretas de direcciones de host.](acting-as-a-host-address-book-provider.md)  <br/> |
|Desplazamiento de prefijos  <br/> |Admitir restricciones en tablas de contenido de contenedor. Para obtener más información, vea [Acerca de las restricciones](about-restrictions.md).  <br/> |
|Búsqueda avanzada en un contenedor  <br/> |Admite la **propiedad PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) en contenedores. Para obtener más información, vea [Implementar la búsqueda avanzada.](implementing-advanced-searching.md)  <br/> |
|Notificación de eventos  <br/> |Implemente [los métodos IABLogon::Advise](iablogon-advise.md) [e IABLogon::Unadvise.](iablogon-unadvise.md) Para obtener más información, vea [Notificación de eventos en MAPI](event-notification-in-mapi.md) y Notificación de eventos de soporte [técnico.](supporting-event-notification.md)  <br/> |
   
Para la notificación de eventos, MAPI llamará al método **IABLogon::Advise** cuando un cliente llame a **IAddrBook::Advise** para registrarse para recibir notificaciones en cualquiera de sus contenedores, usuarios de mensajería o listas de distribución. Sin embargo, dado que la notificación de eventos auxiliar es opcional, puedes devolver MAPI_E_NO_SUPPORT de estos métodos. Sin embargo, MAPI recomienda que al menos admita notificaciones en las tablas de contenido y le anima a admitir todos los tipos de notificación de objetos, excepto  _fnevSearchComplete_ y el evento  _fnevCriticalError_ para agregar valor. 
  

