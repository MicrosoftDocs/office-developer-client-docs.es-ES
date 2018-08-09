---
title: Tablas puntuales
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
description: 'Última modificación: 08 de noviembre de 2011'
ms.openlocfilehash: 3ad9141f2530e64664a2d0c75ece2b834cc6ad78
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818421"
---
# <a name="one-off-tables"></a>Tablas puntuales

**Hace referencia a**: Outlook 
  
Una tabla de uso único contiene información acerca de las plantillas que es compatible con un proveedor de la libreta de direcciones para la creación de nuevos destinatarios. Tablas de uso único se implementan por proveedores de libreta de direcciones, los contenedores de la libreta de direcciones individuales y por MAPI y pueden ser persistentes o temporales. 
  
> [!NOTE]
> Es importante no confundir las plantillas en las tablas de uso único con identificadores de plantilla; Aunque sus objetivos son similares, sus construcciones de código son nada por igual. Las plantillas se usan para crear a los destinatarios de un tipo determinado mientras identificadores de plantilla se utilizan para enlazar los datos de un destinatario que pertenecen a un proveedor de host con código para admitir a otro destinatario que pertenecen a un proveedor externo. 
  
Los clientes de creación a nuevos destinatarios:
  
- Para agregar a la lista de destinatarios de un mensaje saliente.
    
- Para agregar a uno de los contenedores en la libreta de direcciones.
    
En ambos escenarios, se pide un proveedor de la libreta de direcciones para devolver una tabla de uso único. Los proveedores de la libreta de direcciones pueden implementar en una sola tabla de uso único que se utilizará en las situaciones o una tabla de uso único única para cada situación. 
  
Cuando el destinatario se incluirán con un mensaje saliente, MAPI llama al método [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) del proveedor de libreta de direcciones para recuperar su tabla de uso único. En la tabla de uso único incluye plantillas que permiten a un usuario escribir información resultante de la creación de un destinatario con una dirección válida. Registros MAPI para las notificaciones en esta tabla, manteniéndolo abren por lo que pueden reflejarán los cambios al usuario. MAPI libera la tabla sólo cuando se llama a su subsistema o la dirección de la libreta estado método del objeto [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . 
  
Cuando el destinatario se agregarán a un contenedor, MAPI realiza una llamada diferente, invocar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor para recuperar su propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). El conjunto de plantillas que se incluyen en la tabla de uso único representa los tipos de destinatarios que se pueden agregar al contenedor. Por ejemplo, los servidores de correo a menudo exponen un contenedor para cada puerta de enlace que se instala de forma que cada contenedor sólo contiene las direcciones específicas de la puerta de enlace correspondiente.
  
MAPI proporciona una tabla de uso único que incluye su propio plantillas, así como las plantillas de cada uno de los proveedores de la libreta de direcciones en la sesión. MAPI proporciona una plantilla genérica que se puede usar para crear a un nuevo destinatario para cualquier tipo de dirección, suponiendo que el usuario conoce su formato. Los proveedores de la libreta de direcciones Utilice esta tabla de uso único mediante una llamada a [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md). Cada una de las plantillas incluidas en los resultados de la tabla de uso único de MAPI en la creación de los destinatarios con direcciones de destinatario válidos.
  
Normalmente, los proveedores de la libreta de direcciones proporcionan una plantilla para cada tipo de dirección que admiten. Sin embargo, la compatibilidad con las plantillas no es necesario. Los proveedores de la libreta de direcciones que no permitir la creación de nuevas direcciones pueden devolver MAPI_E_NO_SUPPORT cuando llama a MAPI para solicitar una tabla de uso único. Los proveedores de la libreta de direcciones que permite la creación de dirección nueva pero no proporcionan ninguna plantilla pueden llamar a **IMAPISupport::GetOneOffTable** para usar las plantillas que aparecen en la tabla de uso único de MAPI. 
  
Las siguientes propiedades que conforman la columna requiere establecer en las tablas de uso único:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md))
    
 **PR_ADDRTYPE** indica el tipo de dirección que se puede asociar con el nuevo destinatario creado con la plantilla. 
  
 **PR_DISPLAY_NAME** y **PR_DISPLAY_TYPE** asociación datos con el nuevo destinatario. **PR_DISPLAY_NAME** contiene una cadena de caracteres que identifica al nuevo destinatario y **PR_DISPLAY_TYPE** contiene una constante que identifica el tipo de icono que se muestra con la fila. Las plantillas para los usuarios de mensajería tienen su columna **PR_DISPLAY_TYPE** establecida en DT_MAILUSER; las plantillas de listas de distribución tienen su columna **PR_DISPLAY_TYPE** establecida en DT_DISTLIST. 
  
 **Entrada del objeto** es el identificador de entrada de la plantilla que se usará para crear a un nuevo destinatario. Este identificador de entrada se puede pasar a futuras llamadas [IAddrBook::NewEntry](iaddrbook-newentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md)y [IABContainer::CreateEntry](iabcontainer-createentry.md) . Contenedores de establecen la columna de **entrada del objeto** de su fila para la plantilla de usuario para **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) y la columna de **entrada del objeto** de su fila para la lista de distribución predeterminada de mensajería predeterminada plantilla de **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). 
  
 **PR_DEPTH** se utiliza para admitir la visualización jerárquica de las entradas en una tabla de uso único de forma que indica el nivel de sangría de la plantilla. Aunque las tablas de uso único se pueden mostrar como una lista plana o una presentación jerárquica, este último es preferible y los proveedores de la libreta de direcciones deben admitir estableciendo la columna **PR_DEPTH** para cada fila de forma adecuada. **PR_DEPTH** está basada en cero; las filas con un valor de 0 en la columna **PR_DEPTH** no se aplica sangría. Cuanto mayor sea el valor de **PR_DEPTH**, la fila es con sangría. Por ejemplo, filas con **PR_DEPTH** establecida en 1 son una ficha con sangría mientras filas con **PR_DEPTH** establecido en 3 son tres fichas con sangría. 
  
 **PR_SELECTABLE** se usa para indicar si una fila en la tabla representa una plantilla que se puede seleccionar y usa para crear a un nuevo destinatario. Aunque la mayoría de las filas en una tabla de uso único representan plantillas, proveedores pueden incluir las filas que no son de plantilla. Por ejemplo, es posible que un proveedor de desee organizar de la tabla de uso único por tipo de plantilla, incluida una fila de categoría que aparece en la pantalla, pero no se usa para la creación de destinatarios. 
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

