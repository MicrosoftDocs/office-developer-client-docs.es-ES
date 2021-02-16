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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428371"
---
# <a name="hierarchy-tables"></a>Tablas de jerarquía

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla de jerarquía contiene información sobre las carpetas de un almacén de mensajes o los contenedores de un contenedor de libreta de direcciones. Cada fila de una tabla de jerarquía contiene un conjunto de columnas con información acerca de una carpeta o contenedor de libreta de direcciones. Las tablas de jerarquía son usadas principalmente por los clientes e implementadas por los proveedores de almacén de mensajes para mostrar un árbol de carpetas y subcarpetas e implementadas por proveedores de libretas de direcciones para mostrar un árbol de contenedores en la libreta de direcciones. Los contenedores que no pueden contener subcontenedores, como se indica por la ausencia de la marca AB_SUBCONTAINERS en su propiedad **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)), no implementan una tabla de jerarquía.
  
Se puede tener acceso a una tabla de jerarquía llamando a:
  
- [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).
    
    - O bien:
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pasando **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) como la etiqueta de propiedad y IID_IMAPITable como identificador de interfaz.
    
Los contenedores y las carpetas deben admitir ambas técnicas para recuperar propiedades de tabla. No es aceptable que los proveedores de servicios admitan solo una forma de obtener acceso a estas tablas porque los clientes esperan tener la opción. 
  
> [!IMPORTANT]
> No se garantiza que los proveedores de almacén respetarán el conjunto de criterios de ordenación especificado para las tablas de jerarquía. 
  
La llamada a **IMAPIProp::OpenProperty** implica tener acceso a la tabla de jerarquía abriendo su propiedad correspondiente, **PR_CONTAINER_HIERARCHY**. Aunque **PR_CONTAINER_HIERARCHY** se puede recuperar a través del método [IMAPIProp::GetProps](imapiprop-getprops.md) de una carpeta o contenedor, se incluye en la matriz de etiquetas de propiedades que devuelve el método [IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
  
 **PR_CONTAINER_HIERARCHY** puede usarse para incluir o excluir una tabla de jerarquía de una operación de copia. Si un cliente  especifica PR_CONTAINER_HIERARCHY en el parámetro *lpExcludeProps* para [IMAPIProp::CopyTo](imapiprop-copyto.md) en una operación de copia, la nueva carpeta o contenedor no admitirá la tabla de jerarquía de la carpeta o contenedor original. 
  
Las siguientes propiedades son la columna necesaria establecida en una tabla de jerarquía:
  
|||
|:-----|:-----|
|**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** contiene el nombre del contenedor o carpeta que debe aparecer en la presentación de la jerarquía. 
  
 **PR_ENTRYID** es el identificador de entrada asociado a este contenedor o carpeta. Se espera que sea un identificador de entrada a largo plazo. Los clientes y MAPI pueden pasar este identificador de entrada **a OpenEntry** para abrir el contenedor o carpeta y ver su contenido llamando a [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md). 
  
 **PR_DEPTH** es un valor numérico que indica el nivel de sangría de este contenedor o carpeta en el que cero es el nivel superior. Cuanto más profundo se encuentra en la jerarquía un contenedor o carpeta, mayor será el valor de **su PR_DEPTH** propiedad. Los clientes usan **PR_DEPTH** propiedad para mostrar una tabla de jerarquía adecuadamente para que los usuarios puedan ver claramente las relaciones primarias y secundarias. La profundidad del contenedor o carpeta siempre es relativa al contenedor o carpeta que implementa la tabla de jerarquía. 
  
 **PR_OBJECT_TYPE** siempre se establece en MAPI_ABCONT para tablas de jerarquía de libretas de direcciones y MAPI_FOLDER para tablas de jerarquía de carpetas. 
  
 **PR_DISPLAY_TYPE** es un valor numérico relacionado con cómo se muestra un contenedor o carpeta en la tabla de jerarquía. Se usa principalmente con fines de visualización, para diferenciar visualmente entre tipos de contenedores o carpetas. Muchos proveedores de almacén de mensajes y libreta de direcciones usan iconos para los distintos tipos de presentación. Es el proveedor el que debe proporcionar estos iconos; MAPI no proporciona valores predeterminados. 
  
MAPI define muchos valores para **PR_DISPLAY_TYPE**, algunos que son válidos para carpetas y otros que se usan con las tablas de jerarquía de contenedores de libreta de direcciones. Normalmente, el PR_DISPLAY_TYPE  de una carpeta se establece en DT_FOLDER para indicar un icono de carpeta predeterminado, DT_FOLDER_LINK para indicar un icono que representa un vínculo a otra carpeta o DT_FOLDER_SPECIAL para indicar un icono específico de la aplicación. DT_FOLDER_LINK se usa con carpetas de resultados de búsqueda. 
  
Además de estas columnas necesarias, las tablas de jerarquía de la libreta de direcciones deben incluir **la PR_CONTAINER_FLAGS** propiedad. **PR_CONTAINER_FLAGS** indica varios atributos acerca de un contenedor en la jerarquía y se usa para distinguir un contenedor de otro. 
  
Una propiedad opcional para las tablas de jerarquía de la libreta de direcciones **es PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)).
  
Las tablas de jerarquía del almacén de mensajes incluyen estas propiedades en su conjunto de columnas requerido:
  
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
Los proveedores de libretas de direcciones deben admitir los siguientes **métodos IMAPITable** en sus implementaciones de tabla de jerarquía, ya que son necesarios para la libreta de direcciones integrada de MAPI: 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>Consulte también



[Tablas MAPI](mapi-tables.md)

