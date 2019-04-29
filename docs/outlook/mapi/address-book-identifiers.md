---
title: Identificadores de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 40f6c699-86aa-4324-a30d-12c8f1e2de9c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 822d83c4b77d06c2e000b391c7e229985470ccd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421574"
---
# <a name="address-book-identifiers"></a>Identificadores de la libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Todos los proveedores de la libreta de direcciones asignan **** identificadores de entrada usando la propiedad[PidTagEntryId](pidtagentryid-canonical-property.md)) a sus objetos de mensajería y de lista de distribución. Las aplicaciones cliente usan estos identificadores de entrada para abrir y tener acceso a los objetos a los que están asignados.
  
La libreta de direcciones utiliza otros tres tipos de identificadores para representar objetos:
  
- Identificadores de entrada puntuales
    
- Identificadores de entrada de plantilla de un solo uso
    
- Identificadores de plantilla
    
Debido a la variedad de identificadores de entrada y a la similitud con la que se les asigna un nombre, es fácil confundirse sobre cómo se usa y crea cada tipo. 
  
Un identificador de entrada de un solo uso es un identificador de entrada que se usa para abrir y tener acceso al tipo de destinatario conocido como destinatario único o personalizado. Las cancelaciones son destinatarios que no pertenecen a ninguno de los proveedores de la libreta de direcciones en el perfil. Los identificadores de entrada asignados a una sola vez usan un formato reservado específicamente para destinatarios de uso único. Como los identificadores de entrada de un solo uso se usan para abrir objetos y obtener acceso a ellos, se almacenan en la propiedad del usuario.
  
Se crean identificadores de entrada de una sola vez y de uso único:
  
- Cuando los usuarios de una aplicación cliente eligen agregar un destinatario que no representa ninguna entrada de la libreta de direcciones a la lista de destinatarios de un mensaje.
    
- Cuando los usuarios de una aplicación cliente eligen agregar un destinatario que no representa ninguna entrada de la libreta de direcciones a un contenedor de libretas de direcciones modificable.
    
- Cuando un proveedor de transporte recibe un mensaje con una dirección que el proveedor de la libreta de direcciones relacionado no puede controlar.
    
- Cuando un proveedor de transporte recibe un mensaje con una dirección que pertenece a una puerta de enlace.
    
En las dos primeras situaciones, el cliente llama a **IAddrBook:: CreateOneOff** para asociar un identificador de entrada único con el destinatario único creado recientemente. En las dos segunda situaciones, el proveedor de transporte llama a **IMAPISupport:: CreateOneOff** para asociar un identificador de entrada único con la dirección externa. Para obtener más información, vea [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) y [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md).
  
Un identificador de entrada de plantilla de un solo uso es un identificador de entrada a corto plazo que se usa para abrir y tener acceso a una plantilla para crear una o varias desventajas. Proveedores de libretas de direcciones y plantillas de suministro MAPI para escribir la información necesaria para crear un destinatario de un tipo determinado. La información sobre estas plantillas, incluidos sus identificadores de entrada, se publica en la tabla de uso único. Las tablas de uso único se muestran cuando MAPI llama al método **IABLogon:: GetOneOffTable** o a un método **IMAPIProp:: OpenProperty** de un contenedor de libreta de direcciones para solicitar el **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). o cuando un proveedor llama a **IMAPISupport:: GetOneOffTable**. Para obtener más información, vea [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md), [IMAPIProp:: OpenProperty](imapiprop-openproperty.md)y [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md).
  
Para crear un nuevo usuario, seleccione una de las plantillas enumeradas en la tabla de uso único. El cliente pasa la columna 1 de la fila seleccionada, que es el identificador de entrada de plantilla de un solo uso de la plantilla seleccionada, a **IAddrBook:: NEWENTRY** en el parámetro _lpEIDNewEntryTpl_ . Para obtener más información, vea [IAddrBook:: NEWENTRY](iaddrbook-newentry.md). MAPI usa el identificador de entrada de plantilla de un solo uso para mostrar la plantilla y para permitir al usuario escribir la información necesaria para crear el destinatario. 
  
Un identificador de plantilla es un identificador de entrada que algunos proveedores de la libreta de direcciones asignan a sus destinatarios, además del identificador de entrada que se conserva en la propiedad de. Los proveedores establecen la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de un destinatario para almacenar su identificador de plantilla. Algunos proveedores de libretas de direcciones asignan el mismo valor para las propiedades del identificador de entrada y del identificador de plantilla de un destinatario.
  
Los identificadores de plantilla solo los utilizan los proveedores de libreta de direcciones y MAPI para enlazar los datos de los destinatarios en un proveedor, denominado proveedor de host, para codificar el destinatario en otro proveedor, denominado proveedor externo. El proveedor de host proporciona el almacenamiento para el destinatario; el proveedor externo proporciona la lógica. El proceso de enlace permite a un proveedor de host actualizar los datos de un destinatario que almacena mediante el código de un proveedor externo.
  
Cuando el proveedor de hosts está preparado para modificar su destinatario, pasa la propiedad PR_TEMPLATEID en una llamada al método **IMAPISupport:: OpenTemplateID** para iniciar el proceso de enlace. MAPI sigue el proceso mediante la transferencia del identificador de la plantilla al proveedor externo correspondiente a través de una llamada a su método **IABLogon:: OpenTemplateID** . Para obtener más información, vea [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) y [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md). El proveedor externo devuelve un puntero a su implementación de **IMAPIProp** para el destinatario, que el proveedor de host puede usar en vez de su propia implementación. 
  

