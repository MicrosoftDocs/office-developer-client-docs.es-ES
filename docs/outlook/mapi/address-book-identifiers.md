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
ms.openlocfilehash: f9ba7a2a0752dea353e914aaa14a09046b993e5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580526"
---
# <a name="address-book-identifiers"></a>Identificadores de la libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Todos los proveedores de libreta de direcciones asignan los identificadores de entrada mediante la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) para el usuario de mensajería y de objetos de la lista de distribución. Las aplicaciones cliente usan estos identificadores de entrada para abrir y obtener acceso a los objetos a los que se les asignaron.
  
La libreta de direcciones utiliza otros tres tipos de identificadores para representar los objetos:
  
- Identificadores de entrada único
    
- Identificadores de entrada de plantilla de uso único
    
- Identificadores de plantilla
    
Debido a la variedad de los identificadores de entrada y la similitud con la que se denominan, es fácil confundir acerca de cómo se usa y creado cada tipo. 
  
Un identificador de entrada único es un identificador de entrada que se utiliza para abrir y obtener acceso al tipo de destinatario conocido como uso único o el destinatario personalizado. Uso único es los destinatarios que no pertenezcan a cualquiera de los proveedores de la libreta de direcciones en el perfil. Los identificadores de entrada asignados a uso único usan un formato específicamente reservada para los destinatarios de uso único. Debido a que los identificadores de entrada único se usan para abrir y obtener acceso a objetos, están almacenados en la propiedad de entrada del objeto.
  
Se crean identificadores de entrada único y de uso único:
  
- Cuando los usuarios de una aplicación cliente eligen agregar a un destinatario que no representa ninguna entrada en la libreta de direcciones a la lista de destinatarios de un mensaje.
    
- Cuando los usuarios de una aplicación cliente eligen agregar a un destinatario que no representa ninguna entrada en la libreta de direcciones a un contenedor de la libreta de direcciones modificable.
    
- Cuando un proveedor de transporte recibe un mensaje con una dirección que no puede ser tratado por su proveedor de libreta de direcciones relacionados.
    
- Cuando un proveedor de transporte recibe un mensaje con una dirección que pertenece a una puerta de enlace.
    
En los dos primeros casos, el cliente llama a **IAddrBook::CreateOneOff** para asociar un identificador de entrada único con el destinatario de uso único recién creado. En los dos casos, el proveedor de transporte llama a **IMAPISupport::CreateOneOff** para asociar un identificador de entrada único con la dirección externa. Para obtener más información, vea [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) y [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).
  
Un identificador de plantilla de uso único de entrada es un identificador de entrada a corto plazo que se utiliza para abrir y obtener acceso a una plantilla para la creación de uso único. Los proveedores de la libreta de direcciones y MAPI proporcionan plantillas para escribir la información que se necesita para crear a un destinatario de un tipo determinado. Información acerca de estas plantillas, incluidos sus identificadores de entrada, se publica en la tabla de uso único. Tablas de uso único se muestran cuando MAPI llama el método **IABLogon::GetOneOffTable** o **IMAPIProp::OpenProperty** (método) de un contenedor de la libreta de direcciones para solicitar la **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) propiedad o cuando un proveedor llama a **IMAPISupport::GetOneOffTable**. Para obtener más información, vea [IABLogon::GetOneOffTable](iablogon-getoneofftable.md), [IMAPIProp::OpenProperty](imapiprop-openproperty.md)y [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md).
  
Para crear una nueva de uso único, un usuario selecciona una de las plantillas que aparecen en la tabla de uso único. El cliente pasa la columna de entrada del objeto de la fila seleccionada, que es el identificador de entrada de plantilla de uso único de la plantilla seleccionada, al **IAddrBook::NewEntry** en el parámetro _lpEIDNewEntryTpl_ . Para obtener más información, vea [IAddrBook::NewEntry](iaddrbook-newentry.md). MAPI utiliza el identificador de entrada de plantilla de uso único para la plantilla para mostrar y para permitir al usuario que escriba la información necesaria para crear al destinatario. 
  
Un identificador de plantilla es un identificador de entrada que algunos proveedores de libreta de direcciones que se asignan a sus destinatarios además del identificador de entrada que se mantiene en la propiedad de entrada del objeto. Proveedores de establecen la propiedad de **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de un destinatario para almacenar su identificador de plantilla. Algunos proveedores de libreta de direcciones asignan el mismo valor de identificador de plantilla de un destinatario y las propiedades del identificador de entrada.
  
Identificadores de plantilla se usa sólo por los proveedores de la libreta de direcciones y en MAPI para enlazar datos de destinatarios en un proveedor de, conoce como el proveedor de host, para el código para el destinatario en otro proveedor, conoce como el proveedor externo. El proveedor de host proporciona el almacenamiento para el destinatario; el proveedor externo proporciona la lógica. El proceso de enlace permite que un proveedor de host actualizar los datos de un destinatario que almacena con el código de un proveedor externo.
  
Cuando esté listo para modificar a su destinatario el proveedor de host, se pasa la propiedad PR_TEMPLATEID en una llamada al método **IMAPISupport::OpenTemplateID** para iniciar el proceso de enlace. MAPI continúa con el proceso de transferir el identificador de plantilla al proveedor adecuado de externo a través de una llamada a su método **IABLogon::OpenTemplateID** . Para obtener más información, vea [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) y [IABLogon::OpenTemplateID](iablogon-opentemplateid.md). El proveedor externo devuelve un puntero a su implementación de **IMAPIProp** para el destinatario, que puede usar el proveedor de host en lugar de su propia implementación. 
  

