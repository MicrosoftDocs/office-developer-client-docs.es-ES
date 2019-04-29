---
title: Características opcionales para los proveedores de libreta de direcciones
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
# <a name="optional-features-for-address-book-providers"></a>Características opcionales para los proveedores de libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hay muchas características opcionales para los proveedores de la libreta de direcciones. Entre las características que se implementan con más frecuencia se incluyen:
  
- Actuar como proveedor externo permitiendo que las entradas de uno de los contenedores se agreguen al contenedor de otro proveedor.
    
- Actuar como proveedor de host agregando entradas de otro proveedor a uno de los contenedores.
    
- Búsqueda avanzada.
    
- PreFijo de desplazamiento a través de tablas de contenido.
    
- Compatibilidad con listas de distribución.
    
- Compatibilidad con la notificación de eventos.
    
En la tabla siguiente se describen brevemente estas características opcionales y cómo implementarlas:
  
|**Característica**|**Cómo implementar**|
|:-----|:-----|
|Proporcionar plantillas para crear entradas para listas de destinatarios de mensajes  <br/> |Implemente el método [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) . Para obtener más información, vea [tablas de uso único](one-off-tables.md) e [implementación de tablas de un solo uso](implementing-one-off-tables.md).  <br/> |
|Destinatarios de grupo en una unidad con nombre  <br/> |Admitir las propiedades de las listas de distribución mediante la implementación de la interfaz [IDistList: IMAPIContainer](idistlistimapicontainer.md) .  <br/> |
|Actuar como proveedor de libreta de direcciones externa permitiendo agregar entradas a un contenedor de otro proveedor  <br/> | Admitir el enlace de código a datos en el proveedor de host mediante:  <br/>  Compatibilidad con la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) en usuarios de mensajería y listas de distribución. Para obtener más información, consulte identificadores de la [Libreta de direcciones](address-book-identifiers.md).  <br/>  Implementar el método [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) . Para obtener más información, vea [actuar como un proveedor de libreta de direcciones externa](acting-as-a-foreign-address-book-provider.md).  <br/> |
|Actuar como proveedor de la libreta de direcciones de host mediante la inserción de entradas desde otro proveedor  <br/> |Admitir el enlace de datos con el código de un proveedor externo llamando al método [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) . Para obtener más información, consulte [actuar como un proveedor de la libreta de direcciones de host](acting-as-a-host-address-book-provider.md).  <br/> |
|Desplazamiento de preFijo  <br/> |Restricciones de compatibilidad en las tablas de contenido del contenedor. Para obtener más información, consulte [acerca de las restricciones](about-restrictions.md).  <br/> |
|Búsqueda avanzada en un contenedor  <br/> |Admitir la propiedad **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) en los contenedores. Para obtener más información, consulte [implementación de búsqueda avanzada](implementing-advanced-searching.md).  <br/> |
|Notificación de eventos  <br/> |Implemente los métodos [IABLogon:: Advise](iablogon-advise.md) y [IABLogon:: Unadvise](iablogon-unadvise.md) . Para obtener más información, consulte [notificación de eventos en MAPI](event-notification-in-mapi.md) y notificación de [eventos de soporte](supporting-event-notification.md).  <br/> |
   
Para la notificación de eventos, MAPI llamará a su método **IABLogon:: Advise** cuando un cliente llame a **IAddrBook:: Advise** para registrarse en el caso de las notificaciones en uno de los contenedores, los usuarios de mensajería o las listas de distribución. Sin embargo, como la notificación de eventos auxiliar es opcional, puede devolver MAPI_E_NO_SUPPORT de estos métodos. Sin embargo, MAPI recomienda que, al menos, admita notificaciones en las tablas de contenido y le anima a que admita todos los tipos de notificaciones de objeto excepto _fnevSearchComplete_ y el evento _fnevCriticalError_ para agregar valor. 
  

