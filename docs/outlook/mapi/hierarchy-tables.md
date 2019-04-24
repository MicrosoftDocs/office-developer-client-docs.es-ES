---
title: Tablas de jerarquía
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8aa6b36-d6e5-4e1f-8ac5-5d6a78a70bf8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2a1461f0c7196cd425d9736f5837b742bedd4fb5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344581"
---
# <a name="hierarchy-tables"></a>Tablas de jerarquía

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla de jerarquía contiene información sobre las carpetas de un almacén de mensajes o los contenedores de un contenedor de libretas de direcciones. Cada fila de una tabla de jerarquía contiene un conjunto de columnas con información sobre una carpeta o un contenedor de libretas de direcciones. Las tablas de jerarquías las usan principalmente los clientes y las implementan los proveedores de almacenamiento de mensajes para mostrar un árbol de carpetas y subcarpetas, e implementadas por los proveedores de la libreta de direcciones para mostrar un árbol de contenedores en la libreta de direcciones. Los contenedores que no pueden contener subcontenedores, tal y como indica la ausencia de la marca AB_SUBCONTAINERS en su propiedad **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)), no implementan una tabla de jerarquía.
  
Se puede tener acceso a una tabla de jerarquía llamando a:
  
- [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md).
    
    - O
    
- [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) pasando **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) como etiqueta de propiedad y IID_IMAPITable como identificador de interfaz.
    
Los contenedores y las carpetas deben admitir ambas técnicas para recuperar las propiedades de la tabla. No es aceptable que los proveedores de servicios admitan una sola forma de acceso a estas tablas porque los clientes esperan tener la elección. 
  
> [!IMPORTANT]
> No se garantiza que los proveedores de almacenamiento respeten el conjunto de criterio de ordenación especificado para las tablas de jerarquía. 
  
La llamada a **IMAPIProp:: OpenProperty** implica el acceso a la tabla de jerarquía mediante la apertura de la propiedad correspondiente, **PR_CONTAINER_HIERARCHY**. Aunque **PR_CONTAINER_HIERARCHY** no se puede recuperar a través de un método [IMAPIProp:: GetProps](imapiprop-getprops.md) de una carpeta o un contenedor, se incluye en la matriz de etiquetas de propiedad devuelta por el método [IMAPIProp:: GetPropList](imapiprop-getproplist.md) . 
  
 **PR_CONTAINER_HIERARCHY** también se puede usar para incluir o excluir una tabla de jerarquías de una operación de copia. Si un cliente especifica **PR_CONTAINER_HIERARCHY** en el parámetro *lpExcludeProps* para [IMAPIProp:: CopyTo](imapiprop-copyto.md) en una operación de copia, el contenedor o la nueva carpeta no admitirá la tabla de jerarquías del contenedor o la carpeta originales. 
  
Las siguientes propiedades componen el conjunto de columnas necesario en una tabla de jerarquía:
  
|||
|:-----|:-----|
|**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**** Es ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** contiene el nombre del contenedor o la carpeta que debe aparecer en la visualización de la jerarquía. 
  
 **** Valor es el identificador de entrada asociado a este contenedor o carpeta. Se espera que sea un identificador de entrada a largo plazo. Los clientes y MAPI pueden pasar este identificador de entrada a **OpenEntry** para abrir el contenedor o la carpeta y ver su contenido llamando a [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md). 
  
 **PR_DEPTH** es un valor numérico que indica el nivel de sangría de este contenedor o carpeta cuyo nivel superior es cero. Cuanto más profundo esté en la jerarquía, el contenedor o la carpeta, mayor será el valor de su propiedad **PR_DEPTH** . Los clientes usan la propiedad **PR_DEPTH** para mostrar una tabla de jerarquía de forma adecuada para que los usuarios puedan ver claramente las relaciones entre los elementos primarios y secundarios. La profundidad de la carpeta o del contenedor siempre está relacionada con el contenedor o la carpeta que implementa la tabla de jerarquías. 
  
 **PR_OBJECT_TYPE** siempre se establece en MAPI_ABCONT para las tablas y MAPI_FOLDER de jerarquía de la libreta de direcciones para las tablas de jerarquía de carpetas. 
  
 **PR_DISPLAY_TYPE** es un valor numérico que hace referencia al modo en que se muestra un contenedor o una carpeta en la tabla de jerarquías. Se usa principalmente con fines de presentación, para diferenciar visualmente entre los tipos de contenedores o carpetas. Muchos proveedores de almacenamiento de mensajes y de libretas de direcciones usan iconos para los distintos tipos de presentación. El proveedor debe proporcionar estos iconos. MAPI no proporciona valores predeterminados. 
  
MAPI define muchos valores para **PR_DISPLAY_TYPE**, algunos que son válidos para las carpetas y otros que se usan con las tablas de jerarquías de los contenedores de la libreta de direcciones. Normalmente, el **PR_DISPLAY_TYPE** de una carpeta se establece en DT_FOLDER para indicar un icono de carpeta predeterminado, DT_FOLDER_LINK para indicar un icono que representa un vínculo a otra carpeta, o DT_FOLDER_SPECIAL para indicar un icono que es específico de la aplicación. DT_FOLDER_LINK se usa con las carpetas de resultados de búsqueda. 
  
Además de estas columnas obligatorias, las tablas de jerarquía de libretas de direcciones deben incluir la propiedad **PR_CONTAINER_FLAGS** . **PR_CONTAINER_FLAGS** indica varios atributos sobre un contenedor de la jerarquía y se usa para distinguir un contenedor de otro. 
  
Una propiedad opcional para las tablas de jerarquía de la libreta de direcciones es la propiedad **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)).
  
Las tablas de jerarquías del almacén de mensajes incluyen estas propiedades en el conjunto de columnas necesario:
  
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
Los proveedores de la libreta de direcciones deben admitir los siguientes métodos **IMAPITable** en sus implementaciones de tabla de jerarquías, ya que son necesarios para la libreta de direcciones integrada de MAPI: 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

