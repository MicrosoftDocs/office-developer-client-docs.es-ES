---
title: Tablas de un solo uso
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
description: 'Última modificación: 8 de noviembre de 2011'
ms.openlocfilehash: 8719536efa9bffb1226f8fb665b912eb872227f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336487"
---
# <a name="one-off-tables"></a>Tablas de un solo uso

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla de uso único contiene información sobre las plantillas que admite un proveedor de libreta de direcciones para crear nuevos destinatarios. Las tablas de uso único las implementan los proveedores de libreta de direcciones, los contenedores de libretas de direcciones individuales y MAPI, y pueden ser persistentes o temporales. 
  
> [!NOTE]
> No confunda las plantillas de las tablas de uso único con los identificadores de plantilla; Aunque sus propósitos son similares, sus construcciones de código no son nada iguales. Las plantillas se usan para crear destinatarios de un tipo determinado, mientras que los identificadores de plantilla se usan para enlazar los datos de un destinatario que pertenece a un proveedor de host con código para admitir a otro destinatario que pertenece a un proveedor externo. 
  
Los clientes crean nuevos destinatarios:
  
- Para agregar a la lista de destinatarios de un mensaje saliente.
    
- Para agregar a uno de los contenedores de la libreta de direcciones.
    
En ambos escenarios, se pide al proveedor de la libreta de direcciones que devuelva una tabla única. Los proveedores de la libreta de direcciones pueden implementar una sola tabla única para usarse en ambas situaciones o en una única tabla única para cada situación. 
  
Cuando el destinatario se incluya con un mensaje saliente, MAPI llama al método [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) del proveedor de la libreta de direcciones para recuperar su tabla de uso único. La tabla de uso único incluye plantillas que permiten a un usuario escribir información que da como resultado la creación de un destinatario con una dirección válida. MAPI registra las notificaciones en esta tabla, manteniéndola abierta para que los cambios puedan reflejarse en el usuario. MAPI sólo libera la tabla cuando se llama al método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) del objeto de estado de la libreta de direcciones o del subsistema. 
  
Cuando el destinatario se agrega a un contenedor, MAPI realiza una llamada diferente y invoca el método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) del contenedor para recuperar su propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). El conjunto de plantillas incluido en esta tabla única representa los tipos de destinatarios que se pueden agregar al contenedor. Por ejemplo, los servidores de correo a menudo exponen un contenedor para cada puerta de enlace que se instala para que cada contenedor solo retenga las direcciones específicas de la puerta de enlace correspondiente.
  
MAPI proporciona una tabla única que incluye sus propias plantillas, así como plantillas de cada uno de los proveedores de la libreta de direcciones de la sesión. MAPI proporciona una plantilla genérica que se puede usar para crear un nuevo destinatario para cualquier tipo de dirección, suponiendo que el usuario sepa su formato. Los proveedores de libreta de direcciones usan esta tabla única llamando a [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md). Cada una de las plantillas incluidas en la tabla de un solo uso de MAPI da como resultado la creación de destinatarios con direcciones de destinatario válidas.
  
Los proveedores de libretas de direcciones suelen proporcionar una plantilla para cada tipo de dirección que admiten. Sin embargo, no es necesario admitir plantillas. Los proveedores de libretas de direcciones que no permiten la creación de direcciones nuevas pueden devolver MAPI_E_NO_SUPPORT cuando las llamadas MAPI para solicitar una tabla de un solo uso. Los proveedores de libretas de direcciones que permiten la creación de nuevas direcciones, pero no proporcionan ninguna plantilla, pueden llamar a **IMAPISupport:: GetOneOffTable** para usar las plantillas enumeradas en la tabla de un solo uso de MAPI. 
  
Las siguientes propiedades componen el conjunto de columnas necesario en las tablas de un solo uso:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **** Es ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md))
    
 **PR_ADDRTYPE** indica el tipo de dirección que se puede asociar con el nuevo destinatario creado con la plantilla. 
  
 **PR_DISPLAY_NAME** y **PR_DISPLAY_TYPE** asocian datos con el nuevo destinatario. **PR_DISPLAY_NAME** contiene una cadena de caracteres que identifica el nuevo destinatario y **PR_DISPLAY_TYPE** contiene una constante que identifica el tipo de icono que se va a mostrar con la fila. Las plantillas para los usuarios de mensajería tienen la columna **PR_DISPLAY_TYPE** establecida en DT_MAILUSER; las plantillas de las listas de distribución tienen su columna **PR_DISPLAY_TYPE** establecida en DT_DISTLIST. 
  
 **** Valor es el identificador de entrada de la plantilla que se va a usar para crear un nuevo destinatario. Este identificador de entrada se puede pasar a futuras llamadas [IAddrBook:: NEWENTRY](iaddrbook-newentry.md), [IAddrBook:: OpenEntry](iaddrbook-openentry.md)y [IABContainer:: CreateEntry](iabcontainer-createentry.md) . Los contenedores establecen **** la columna de lista de la fila de la plantilla de usuario de mensajería predeterminada en **PR_DEF_CREATE_MAILUSER** ( **** [PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) y la columna de de su fila para la lista de distribución predeterminada. plantilla a **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). 
  
 **PR_DEPTH** se usa para admitir la visualización jerárquica de las entradas de una tabla de uso único indicando el nivel de sangría de la plantilla. Aunque las tablas de uso único se pueden mostrar como una lista plana o como una visualización jerárquica, es preferible y los proveedores de libreta de direcciones deben admitirla si se establece la columna **PR_DEPTH** para cada fila de forma adecuada. **PR_DEPTH** es de base cero; las filas con un valor de 0 en la columna **PR_DEPTH** no tienen sangría. Cuanto mayor sea el valor de **PR_DEPTH**, mayor será la sangría que se aplicará a la fila. Por ejemplo, las filas con **PR_DEPTH** establecido en 1 tienen aplicada una sangría de una tabulación, mientras que las filas con **PR_DEPTH** establecido en 3 tienen tres fichas con sangría. 
  
 **PR_SELECTABLE** se usa para indicar si una fila de la tabla representa una plantilla que se puede seleccionar y usar para crear un nuevo destinatario. Aunque la mayoría de las filas de una tabla de uso único representan plantillas, los proveedores pueden incluir filas que no sean plantillas. Por ejemplo, es posible que un proveedor desee organizar la tabla de uso único por tipo de plantilla, incluida una fila de categoría que aparece en la presentación pero que no se usa para la creación de destinatarios. 
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

