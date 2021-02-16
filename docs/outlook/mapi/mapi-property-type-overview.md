---
title: Información general sobre el tipo de propiedad MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b762f5fb-7c2c-4303-96f7-0b6e657146c9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 58dd25f09b76d97fd6441915225756a19f4ec3cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438200"
---
# <a name="mapi-property-type-overview"></a>Información general sobre el tipo de propiedad MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los tipos de propiedad son constantes definidas por MAPI en MAPIDEFS. Archivo de encabezado H que indica el tipo de datos subyacente de un valor de propiedad. Todas las propiedades, ya sean definidas por MAPI, por aplicaciones cliente o por proveedores de servicios, usan uno de estos tipos. 
  
Los tipos de propiedad siguen una convención de nomenclatura similar a la que se usa para las etiquetas de propiedad. Muchos tipos de propiedades tienen una versión de valor único y de varios valores. Las propiedades de un solo valor contienen un valor de su tipo, como un entero único o una cadena de caracteres. La constante usada para representar una propiedad de valor único tiene dos partes: el prefijo PT_ y una cadena que describe el tipo real, como LONG o STRING8. 
  
Las propiedades de varios valores contienen más de un valor de su tipo. A diferencia de las matrices de variante OLE, cada valor de una propiedad multivalor es del mismo tipo. La constante usada para representar propiedades multivalor se crea combinando la marca MV_FLAG con la constante de valor único correspondiente que representa el tipo base. Hay tres partes: el prefijo PT_ seguido de MV_ seguido de una cadena que describe el tipo. Por ejemplo, el tipo de una propiedad que contiene varios enteros es PT_MV_LONG y para varias cadenas de caracteres es PT_MV_STRING8.
  
En la siguiente ilustración se muestra la estructura de una estructura [SPropValue](spropvalue.md) para describir un entero de varios valores, una propiedad de tipo PT_MV_LONG. El **miembro** Value se expande para incluir un recuento del número de valores enteros en la propiedad y un puntero a una matriz de esos valores. 
  
**Propiedades multivalor**
  
![Propiedades de varios valores Propiedades]de varios(media/amapi_12.gif "valores")
  
Aunque la compatibilidad con las propiedades de varios valores es opcional, MAPI recomienda que los clientes y proveedores de servicios admitan ambos tipos de propiedades, ya que al hacerlo, se permite una mayor interacción entre componentes compatibles con MAPI.
  
En la siguiente ilustración se enumeran todas las constantes de tipo de propiedad diferentes, que muestran dónde se almacenan en una **estructura SPropValue.** El tamaño del miembro **Value** depende del tipo en particular. Tenga en cuenta que no todos los tipos de valor único tienen equivalentes de varios valores. 
  
**Constantes de tipo de propiedad**
  
![Constantes de tipo de propiedad Constantes]de tipo de(media/amapi_11.gif "propiedad")
  
Los clientes y proveedores de servicios que trabajan con una propiedad deben seguir dos pasos:
  
1. Determinar si la propiedad está disponible o no.
    
2. Si está disponible, recupere el valor de la propiedad.
    
A veces, un cliente o proveedor de servicios solo necesita comprobar la existencia de una propiedad; otras veces es necesario comprobar si hay un valor específico. Por ejemplo, los proveedores de transporte tienen tres cursos de acción diferentes para procesar la propiedad **PR \_ SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), un valor booleano que indica si un mensaje debe transmitirse con texto con formato. Si **pr \_ SEND_RICH_INFO** se establece en TRUE, el proveedor de transporte transmite el texto con formato. Si se establece en FALSE, el texto con formato se descarta antes de la transmisión. Si **PR_SEND_RICH_INFO** no está disponible, el proveedor de transporte sigue su curso de acción predeterminado, independientemente de lo que sea para el proveedor en particular. 
  
MAPI define un tipo de propiedad especial, PT_UNSPECIFIED, que un cliente o proveedor de servicios puede usar para recuperar una propiedad cuando el tipo de propiedad es desconocido. Para recuperar una propiedad sin conocimiento previo de su tipo, un cliente o proveedor de servicios llama al método [IMAPIProp::GetProps](imapiprop-getprops.md) de un objeto y pasa una etiqueta de propiedad que se compronó con el identificador de la propiedad y el tipo de propiedad PT_UNSPECIFIED. **GetProps devuelve** una [estructura SPropValue](spropvalue.md) para la propiedad, reemplazando PT_UNSPECIFIED por el tipo adecuado. Los proveedores de servicios **que implementan GetProps** son necesarios para admitir PT_UNSPECIFIED. 
  
Algunos objetos MAPI admiten propiedades que son a su vez objetos. Las propiedades del objeto tienen el tipo PT_OBJECT. En lugar de usar **IMAPIProp::GetProps** para tener acceso a estas propiedades, los clientes y proveedores de servicios suelen usar el método [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) especificando la interfaz adecuada para el acceso, o un método en el objeto que admite la propiedad. 
  
Dado que el acceso al valor de una propiedad de objeto implica el uso de una de las interfaces del objeto, **GetProps** no es apropiado. Con **GetProps,** el llamador obtiene acceso al valor de una propiedad a través de una **estructura SPropValue.** Con **IMAPIProp::OpenProperty,** el autor de la llamada recupera un puntero a una interfaz que puede tener acceso al objeto. **OpenProperty** siempre se puede usar para recuperar una propiedad de objeto. La otra opción, llamar a un método en el objeto, no está disponible con todas las propiedades del objeto. 
  
Por ejemplo, cada carpeta admite dos tablas, una tabla de jerarquía y una tabla de contenido. Estas tablas son propiedades de la carpeta; sus etiquetas de **propiedad PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) y **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). Las tablas son objetos que requieren la **interfaz IMAPITable** para el acceso. Un cliente puede llamar al método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) de la carpeta para obtener acceso a la tabla de jerarquía, al método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) de la carpeta para obtener acceso a la tabla de contenido o al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de la carpeta para obtener acceso a cualquiera de las tablas. Para llamar **a OpenProperty**, un cliente pasa la etiqueta de propiedad de la propiedad como primer parámetro y un identificador de interfaz para la interfaz que se usará para el acceso como segundo parámetro. Estos parámetros serían **PR_CONTAINER_HIERARCHY** o **PR_CONTAINER_CONTENTS** y **IID_IMAPITable**.
  
Para obtener una lista completa de los tipos de propiedad de valor único y de varios valores, vea [Tipos de propiedad](property-types.md). 
  
## <a name="see-also"></a>Vea también

- [Información general sobre MAPI (propiedad)](mapi-property-overview.md)

