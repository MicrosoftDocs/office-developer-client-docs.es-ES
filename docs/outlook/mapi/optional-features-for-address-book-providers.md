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
ms.openlocfilehash: ffdd1203316b2c80aba34c980745a0330ec19888
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818448"
---
# <a name="optional-features-for-address-book-providers"></a>Características opcionales para los proveedores de libreta de direcciones

  
  
**Hace referencia a**: Outlook 
  
Existen muchas características opcionales para los proveedores de la libreta de direcciones. Algunas de las características implementadas con más frecuencia son:
  
- Que actúa como un proveedor externo al permitir que las entradas de uno de los contenedores que se agregará al contenedor de otro proveedor.
    
- Actúa como un proveedor de host mediante la adición de entradas de otro proveedor a uno de los contenedores.
    
- La búsqueda avanzada.
    
- Prefijo de desplazamiento a través de tablas de contenido.
    
- Compatibilidad con las listas de distribución.
    
- Compatibilidad con la notificación de eventos.
    
En la siguiente tabla se describe brevemente estas características opcionales y cómo implementarlos:
  
|**Característica**|**Cómo implementar**|
|:-----|:-----|
|Proporcionar plantillas para crear las entradas del mensaje de las listas de destinatarios  <br/> |Implemente el método [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) . Para obtener más información, vea [Implementar constituye tablas](implementing-one-off-tables.md)y [Tablas de uso único](one-off-tables.md) .  <br/> |
|Destinatarios de grupo en una unidad con nombre  <br/> |Admite las propiedades de las listas de distribución mediante la implementación de la [IDistList: IMAPIContainer](idistlistimapicontainer.md) interfaz.  <br/> |
|Actuar como un proveedor de libreta de direcciones externa al permitir que las entradas que se agregarán a un contenedor en otro proveedor  <br/> | Compatibilidad con el código de enlace de datos en el proveedor de host por:  <br/>  Compatibilidad con la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) en los usuarios y las listas de distribución de mensajería. Para obtener más información, vea [Identificadores de la libreta de direcciones](address-book-identifiers.md).  <br/>  Implementación del método [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) . Para obtener más información, vea [actuar como un proveedor de libreta de direcciones externa](acting-as-a-foreign-address-book-provider.md).  <br/> |
|Que actúa como un proveedor de libreta de direcciones de host mediante la inserción de entradas de otro proveedor  <br/> |Admite el enlace de datos en código de un proveedor externo llamando al método [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) . Para obtener más información, vea [actuar como un proveedor de libreta de direcciones de Host](acting-as-a-host-address-book-provider.md).  <br/> |
|Prefijo de desplazamiento  <br/> |Admite restricciones en las tablas de contenido del contenedor. Para obtener más información, vea [Acerca de las restricciones](about-restrictions.md).  <br/> |
|En un contenedor de la búsqueda avanzada  <br/> |Admite la propiedad **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) en los contenedores. Para obtener más información, vea [Implementación avanzada buscar](implementing-advanced-searching.md).  <br/> |
|Notificación de eventos  <br/> |Implementar los métodos [IABLogon::Advise](iablogon-advise.md) y [IABLogon::Unadvise](iablogon-unadvise.md) . Para obtener más información, vea [Compatibilidad con notificación de eventos](supporting-event-notification.md)y [Notificación de eventos en MAPI](event-notification-in-mapi.md) .  <br/> |
   
Para la notificación de eventos, se llamará al método **IABLogon::Advise** por MAPI cuando un cliente llama a **IAddrBook::Advise** para registrar las notificaciones en cualquiera de los contenedores de usuarios o listas de distribución de mensajería. Sin embargo, debido a que la compatibilidad con notificación de evento es opcional, puede devolver MAPI_E_NO_SUPPORT de estos métodos. Sin embargo, MAPI recomienda al menos admitir notificaciones en las tablas de contenido y anima a admitir todos los tipos de notificación de objeto excepto _fnevSearchComplete_ y el evento _fnevCriticalError_ para agregar valor. 
  

