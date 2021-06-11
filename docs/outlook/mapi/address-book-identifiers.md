---
title: Identificadores de libreta de direcciones
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
# <a name="address-book-identifiers"></a>Identificadores de libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Todos los proveedores de libreta de direcciones asignan identificadores de entrada **mediante la** propiedad PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) a sus objetos de lista de distribución y usuario de mensajería. Las aplicaciones cliente usan estos identificadores de entrada para abrir y obtener acceso a los objetos a los que están asignados.
  
La libreta de direcciones usa otros tres tipos de identificadores para representar objetos:
  
- Identificadores de entrada puntuales
    
- Identificadores de entrada de plantilla única
    
- Identificadores de plantilla
    
Debido a la variedad de identificadores de entrada y la similitud con la que se denominan, es fácil confundirse acerca de cómo se usa y crea cada tipo. 
  
Un identificador de entrada único es un identificador de entrada que se usa para abrir y obtener acceso al tipo de destinatario conocido como destinatario único o destinatario personalizado. Los destinatarios únicos son destinatarios que no pertenecen a ninguno de los proveedores de libreta de direcciones del perfil. Los identificadores de entrada asignados a one-offs usan un formato reservado específicamente para destinatarios únicos. Dado que los identificadores de entrada únicos se usan para abrir y obtener acceso a objetos, se almacenan en la PR_ENTRYID única.
  
Se crean identificadores de entrada únicos y únicos:
  
- Cuando los usuarios de una aplicación cliente eligen agregar un destinatario que no representa ninguna entrada de la libreta de direcciones a la lista de destinatarios de un mensaje.
    
- Cuando los usuarios de una aplicación cliente eligen agregar un destinatario que no representa ninguna entrada de la libreta de direcciones a un contenedor modificable de libreta de direcciones.
    
- Cuando un proveedor de transporte recibe un mensaje con una dirección que no puede ser manejada por su proveedor de libreta de direcciones relacionado.
    
- Cuando un proveedor de transporte recibe un mensaje con una dirección que pertenece a una puerta de enlace.
    
En las dos primeras situaciones, el cliente llama a **IAddrBook::CreateOneOff** para asociar un identificador de entrada único con el destinatario único recién creado. En las dos segundas situaciones, el proveedor de transporte llama a **IMAPISupport::CreateOneOff** para asociar un identificador de entrada único con la dirección externa. Para obtener más información, vea [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) e [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).
  
Un identificador de entrada de plantilla único es un identificador de entrada a corto plazo que se usa para abrir y tener acceso a una plantilla para crear uno-offs. Proveedores de libreta de direcciones y plantillas de suministro MAPI para especificar la información necesaria para crear un destinatario de un tipo determinado. La información sobre estas plantillas, incluidos sus identificadores de entrada, se publica en la tabla de un solo elemento. Las tablas de uso único se muestran cuando MAPI llama al método **IABLogon::GetOneOffTable** o al método **IMAPIProp::OpenProperty** de un contenedor de libreta de direcciones para solicitar la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) o cuando un proveedor llama a **IMAPISupport::GetOneOffTable**. Para obtener más información, vea [IABLogon::GetOneOffTable](iablogon-getoneofftable.md), [IMAPIProp::OpenProperty](imapiprop-openproperty.md)e [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md).
  
Para crear un solo uso nuevo, un usuario selecciona una de las plantillas enumeradas en la tabla de uso único. El cliente pasa la columna PR_ENTRYID de la fila seleccionada, que es el identificador de entrada de plantilla única de la plantilla seleccionada, a **IAddrBook::NewEntry en** el parámetro _lpEIDNewEntryTpl._ Para obtener más información, vea [IAddrBook::NewEntry](iaddrbook-newentry.md). MAPI usa el identificador de entrada de plantilla única para mostrar la plantilla y permitir que el usuario escriba la información necesaria para crear el destinatario. 
  
Un identificador de plantilla es un identificador de entrada que algunos proveedores de libreta de direcciones asignan a sus destinatarios, además del identificador de entrada que se mantiene en la PR_ENTRYID principal. Los proveedores establecen la propiedad **PR_TEMPLATEID** de un destinatario ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) para almacenar su identificador de plantilla. Algunos proveedores de libreta de direcciones asignan el mismo valor para el identificador de plantilla de un destinatario y las propiedades del identificador de entrada.
  
Los identificadores de plantilla solo los usan los proveedores de libreta de direcciones y MAPI para enlazar datos de destinatarios en un proveedor, denominado proveedor de host, para codificar el destinatario en otro proveedor, denominado proveedor externo. El proveedor de host proporciona el almacenamiento para el destinatario; el proveedor externo proporciona la lógica. El proceso de enlace permite a un proveedor de host actualizar los datos de un destinatario que almacena mediante el código de un proveedor externo.
  
Cuando el proveedor de host está listo para modificar su destinatario, pasa la propiedad PR_TEMPLATEID en una llamada al método **IMAPISupport::OpenTemplateID** para iniciar el proceso de enlace. MAPI continúa el proceso transfiriendo el identificador de plantilla al proveedor externo correspondiente mediante una llamada a su **método IABLogon::OpenTemplateID.** Para obtener más información, vea [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) e [IABLogon::OpenTemplateID](iablogon-opentemplateid.md). El proveedor externo devuelve un puntero a su **implementación IMAPIProp** para el destinatario, que el proveedor de host puede usar en lugar de su propia implementación. 
  

