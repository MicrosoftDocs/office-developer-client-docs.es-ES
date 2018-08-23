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
ms.openlocfilehash: 2de51e1cf0f29c91e39eb3c6dbaab065fd7d5972
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590529"
---
# <a name="mapi-property-type-overview"></a>Información general sobre el tipo de propiedad MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Tipos de propiedades son constantes definidas por MAPI en el MAPIDEFS. Archivo de encabezado H que indican el tipo de datos subyacente de un valor de la propiedad. Todas las propiedades, si se definen mediante MAPI, por las aplicaciones cliente o por los proveedores de servicio, use uno de estos tipos. 
  
Tipos de propiedad siguen una convención de nomenclatura similar al usado para las etiquetas de propiedad. Muchos tipos de propiedad tienen una versión de valor único y de varios valores. Propiedades de valor único contengan un valor de su tipo como un único número entero o una cadena de caracteres. La constante que se utiliza para representar una propiedad de valor único consta de dos partes: el prefijo PT_ y una cadena que describe el tipo real, como LONG o STRING8. 
  
Propiedades de varios valores contienen más de un valor de su tipo. A diferencia de las matrices variantes OLE, cada valor en una propiedad multivalor es del mismo tipo. La constante que se utiliza para representar las propiedades multivalores se crea mediante la combinación de la marca MV_FLAG con la correspondiente constante de valor de tipo single que representa el tipo base. Hay tres partes: el prefijo PT_ seguido MV_ seguido de una cadena que describe el tipo. Por ejemplo, el tipo de una propiedad que contiene varios enteros es PT_MV_LONG y para varias cadenas de caracteres es PT_MV_STRING8.
  
En la siguiente ilustración muestra la estructura de una estructura [SPropValue](spropvalue.md) para describir un número entero de varios valores, una propiedad de tipo PT_MV_LONG. El **valor** de miembro se expande para incluir un recuento del número de valores enteros en la propiedad y un puntero a una matriz de esos valores. 
  
**Propiedades multivalor**
  
![Propiedades de varios valores] (media/amapi_12.gif "Propiedades de varios valores")
  
Si bien el soporte para varios valores propiedades es opcional, MAPI, se recomienda que los clientes y proveedores de servicios admiten ambos tipos de propiedades porque haciendo es así permite una mayor interacción entre los componentes compatibles con MAPI.
  
En la ilustración siguiente se enumera todas las constantes de tipo de propiedad diferentes, que muestra donde están almacenados en una estructura **SPropValue** . El tamaño del **valor de** miembro es depende del tipo determinado. Tenga en cuenta que no todos los tipos de valor único de tienen equivalentes de varios valores. 
  
**Constantes de tipo de propiedad**
  
![Constantes de tipo (propiedad)] (media/amapi_11.gif "Constantes de tipo (propiedad)")
  
Los clientes y proveedores de servicios de trabajar con una propiedad deben seguir dos pasos:
  
1. Determinar si la propiedad está disponible o no disponible.
    
2. Si está disponible, recuperar el valor de la propiedad.
    
En ocasiones, un proveedor de servicio o cliente sólo necesita comprobar la existencia de una propiedad; otras veces es necesario buscar un valor específico. Por ejemplo, los proveedores de transporte tienen tres cursos diferentes de acción para el procesamiento de la **PR\_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) (propiedad), un valor booleano que indica si un mensaje debe transmitirse con texto con formato. Si **PR\_SEND_RICH_INFO** está establecido en TRUE, el proveedor de transporte transmite el texto con formato. Si se establece en FALSE, se descarta el texto con formato antes de la transmisión. Si **PR_SEND_RICH_INFO** no está disponible, el proveedor de transporte sigue su curso predeterminado de acción, con independencia de es para el proveedor concreto. 
  
MAPI define un tipo de propiedad especial, PT_UNSPECIFIED, que puede usar un proveedor de servicio o cliente para recuperar una propiedad cuando se desconoce el tipo de propiedad. Para recuperar una propiedad sin conocimiento anticipado de su tipo, un proveedor de servicio o cliente llama a un método del objeto [IMAPIProp::GetProps](imapiprop-getprops.md) y pasa una etiqueta de propiedad formada por identificador de la propiedad y el tipo de propiedad PT_UNSPECIFIED. **GetProps** devuelve una estructura [SPropValue](spropvalue.md) para la propiedad, sustituyendo PT_UNSPECIFIED por el tipo adecuado. Proveedores de servicios de implementación de **GetProps** son necesarios para admitir PT_UNSPECIFIED. 
  
Algunos objetos de MAPI admiten propiedades que son los propios objetos. Las propiedades del objeto tengan el tipo de PT Object. En lugar de usar **IMAPIProp::GetProps** para tener acceso a estas propiedades, los clientes y proveedores de servicios de normalmente, el usuario puede ser el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , que especifica la interfaz adecuada para el acceso, o un método en el objeto compatible con la propiedad. 
  
Debido a que el acceso al valor de propiedad de un objeto implica utilizando una de las interfaces para el objeto **GetProps** es inadecuado. Con **GetProps**, el autor de la llamada tiene acceso a un valor de propiedad a través de una estructura **SPropValue** . Con **IMAPIProp::OpenProperty**, el autor de la llamada recupera un puntero a una interfaz que puede tener acceso al objeto. **OpenProperty** siempre puede usarse para recuperar una propiedad de objeto. La otra opción para llamar a un método en el objeto, no está disponible con todas las propiedades de objeto. 
  
Por ejemplo, cada carpeta admite dos tablas, una tabla de jerarquías y una tabla de contenido. Estas tablas son las propiedades de la carpeta; sus etiquetas de propiedad son **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) y **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). Las tablas son objetos que requieren la interfaz **IMAPITable** para el acceso. Un cliente puede llamar al método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) de la carpeta para tener acceso a la tabla de jerarquía (método) [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) de la carpeta para tener acceso a la tabla de contenido, o en la carpeta [IMAPIProp::OpenProperty ](imapiprop-openproperty.md)(método) para tener acceso a cualquiera de ellas. Para llamar a **OpenProperty**, un cliente pasa la etiqueta de propiedad para la propiedad como el primer parámetro y un identificador de interfaz para la interfaz que se utilizará para el acceso como el segundo parámetro. Estos parámetros sería **PR_CONTAINER_HIERARCHY** o **PR_CONTAINER_CONTENTS** y **IID_IMAPITable**.
  
Para obtener una lista completa de los tipos de propiedad de valor único y de varios valores, vea [Tipos de propiedades](property-types.md). 
  
## <a name="see-also"></a>Vea también

- [Información general sobre MAPI (propiedad)](mapi-property-overview.md)

