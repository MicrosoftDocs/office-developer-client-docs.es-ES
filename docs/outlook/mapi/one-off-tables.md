---
title: One-Off tablas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 8719536efa9bffb1226f8fb665b912eb872227f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439530"
---
# <a name="one-off-tables"></a>One-Off tablas

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla de uso único contiene información sobre las plantillas que admite un proveedor de libreta de direcciones para crear nuevos destinatarios. Los proveedores de libretas de direcciones, contenedores individuales de libreta de direcciones y MAPI implementan tablas únicas y pueden ser persistentes o temporales. 
  
> [!NOTE]
> No confunda las plantillas de tablas únicas con identificadores de plantilla; aunque sus propósitos son similares, sus construcciones de código no son iguales. Las plantillas se usan para crear destinatarios de un tipo determinado, mientras que los identificadores de plantilla se usan para enlazar los datos de un destinatario que pertenecen a un proveedor de host con código para admitir otro destinatario que pertenece a un proveedor externo. 
  
Los clientes crean nuevos destinatarios:
  
- Para agregar a la lista de destinatarios de un mensaje saliente.
    
- Para agregar a uno de los contenedores de la libreta de direcciones.
    
En ambos escenarios, se pide a un proveedor de libreta de direcciones que devuelva una tabla de uso único. Los proveedores de libretas de direcciones pueden implementar una única tabla única que se usará en ambas situaciones o una única tabla única para cada situación. 
  
Cuando el destinatario se incluirá con un mensaje saliente, MAPI llama al método [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) del proveedor de libreta de direcciones para recuperar su tabla de uso único. La tabla de uso único incluye plantillas que permiten al usuario escribir información que da como resultado la creación de un destinatario con una dirección válida. MAPI se registra para las notificaciones de esta tabla, manteniéndolo abierto para que los cambios se puedan reflejar en el usuario. MAPI libera la tabla solo cuando se llama al método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) del objeto de estado de la libreta de direcciones o subsistema. 
  
Cuando el destinatario se agregará a un contenedor, MAPI realiza una llamada diferente, invocando el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor para recuperar su propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). El conjunto de plantillas que se incluye en esta tabla de uso único representa los tipos de destinatarios que se pueden agregar al contenedor. Por ejemplo, los servidores de correo suelen exponer un contenedor por cada puerta de enlace instalada de modo que cada contenedor solo contiene direcciones específicas de la puerta de enlace correspondiente.
  
MAPI proporciona una tabla única que incluye sus propias plantillas, así como plantillas de cada uno de los proveedores de libreta de direcciones de la sesión. MAPI proporciona una plantilla genérica que se puede usar para crear un nuevo destinatario para cualquier tipo de dirección, suponiendo que el usuario conoce su formato. Los proveedores de libreta de direcciones usan esta tabla única llamando a [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md). Cada una de las plantillas incluidas en la tabla única MAPI da como resultado la creación de destinatarios con direcciones de destinatarios válidas.
  
Los proveedores de libreta de direcciones suelen proporcionar una plantilla por cada tipo de dirección que admiten. Sin embargo, no es necesario admitir plantillas. Los proveedores de libreta de direcciones que no permiten la creación de nuevas direcciones pueden devolver MAPI_E_NO_SUPPORT cuando MAPI llama para solicitar una tabla de uso único. Los proveedores de libreta de direcciones que permiten la creación de nuevas direcciones pero no suministran ninguna plantilla pueden llamar a **IMAPISupport::GetOneOffTable** para usar las plantillas enumeradas en la tabla de uso único MAPI. 
  
Las siguientes propiedades hacen que la columna necesaria se establezca en tablas únicas:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md))
    
 **PR_ADDRTYPE** indica el tipo de dirección que se puede asociar con el nuevo destinatario creado con la plantilla. 
  
 **PR_DISPLAY_NAME** y **PR_DISPLAY_TYPE** los datos con el nuevo destinatario. **PR_DISPLAY_NAME** contiene una cadena de caracteres que identifica al nuevo destinatario y **PR_DISPLAY_TYPE** contiene una constante que identifica el tipo de icono que se va a mostrar con la fila. Las plantillas para los usuarios de **mensajería tienen su PR_DISPLAY_TYPE** columna establecida en DT_MAILUSER; Las plantillas para listas de distribución **tienen su PR_DISPLAY_TYPE** columna establecida en DT_DISTLIST. 
  
 **PR_ENTRYID** es el identificador de entrada de la plantilla que se usará para crear un nuevo destinatario. Este identificador de entrada se puede pasar a futuras [llamadas IAddrBook::NewEntry](iaddrbook-newentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md)y [IABContainer::CreateEntry.](iabcontainer-createentry.md) Los contenedores establecen la columna **PR_ENTRYID** de su fila para la plantilla de usuario de mensajería predeterminada en **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) y la columna **PR_ENTRYID** de su fila para la plantilla de lista de distribución predeterminada en **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). 
  
 **PR_DEPTH** se usa para admitir la presentación jerárquica de las entradas de una tabla de uso único indicando el nivel de sangría de la plantilla. Aunque las tablas únicas se pueden mostrar como una lista plana o una presentación jerárquica, esta última es preferible y los proveedores de libreta de direcciones deben admitirla estableciendo la columna **PR_DEPTH** para cada fila adecuadamente. **PR_DEPTH** es de base cero; las filas con un valor de 0 en **su PR_DEPTH** no se aplica sangría. Cuanto mayor sea el valor **de PR_DEPTH**, más sangría tiene la fila. Por ejemplo, las filas **con PR_DEPTH** establecidas en 1 se aplica una sangría a una pestaña, mientras que las filas con **PR_DEPTH** establecidas en 3 tienen sangría tres pestañas. 
  
 **PR_SELECTABLE** se usa para indicar si una fila de la tabla representa una plantilla que se puede seleccionar y usar para crear un nuevo destinatario. Aunque la mayoría de las filas de una tabla única representan plantillas, los proveedores pueden incluir filas que no son de plantilla. Por ejemplo, es posible que un proveedor desee organizar la tabla de uso único por tipo de plantilla, incluida una fila de categoría que aparece en la pantalla pero que no se usa para la creación de destinatarios. 
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

