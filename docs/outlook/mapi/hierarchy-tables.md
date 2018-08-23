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
ms.openlocfilehash: d135e0c224866cd2a675df2ef9ec1b206f3169ab
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580757"
---
# <a name="hierarchy-tables"></a>Tablas de jerarquía

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla de jerarquía contiene información acerca de las carpetas en un almacén de mensajes o los contenedores en un contenedor de la libreta de direcciones. Cada fila de una tabla de jerarquía contiene un conjunto de columnas con información acerca de una carpeta o contenedor de la libreta de direcciones. Tablas de jerarquía principalmente son utilizadas por los clientes e implementadas por los proveedores de almacén de mensajes para mostrar un árbol de carpetas y subcarpetas e implementadas por los proveedores de la libreta de direcciones para mostrar un árbol de contenedores en la libreta de direcciones. Contenedores que no se incluyen los subcontenedores, tal como se indica por la ausencia de la marca AB_SUBCONTAINERS en su propiedad **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)), no implementar una tabla de jerarquía.
  
Puede tener acceso a una tabla de jerarquías llamando:
  
- [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).
    
    - O bien -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pasando **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) como la etiqueta de propiedad y IID_IMAPITable como el identificador de interfaz.
    
Contenedores y carpetas deben admitir ambas técnicas para recuperar propiedades de la tabla. Es inaceptable para proveedores de servicios admitir sólo una manera de obtener acceso a estas tablas debido a que los clientes esperan tener la opción. 
  
> [!IMPORTANT]
> No se garantiza que los proveedores de almacén para respetar el criterio de ordenación especificado para tablas de jerarquía. 
  
La llamada a **IMAPIProp::OpenProperty** implica tener acceso a la tabla de jerarquía abriendo su propiedad correspondiente, **PR_CONTAINER_HIERARCHY**. Aunque no se puede recuperar **PR_CONTAINER_HIERARCHY** a través de una carpeta o un método de [IMAPIProp::GetProps](imapiprop-getprops.md) del contenedor, se incluye en la matriz de etiqueta de propiedad que es devuelto por el método [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
  
 **PR_CONTAINER_HIERARCHY** también puede utilizarse para incluir o excluir una tabla de jerarquías de una operación de copia. Si un cliente especifica **PR_CONTAINER_HIERARCHY** en el parámetro *lpExcludeProps* para [IMAPIProp::CopyTo](imapiprop-copyto.md) en una operación de copia, el contenedor o la nueva carpeta no será compatible con la tabla de jerarquía de la carpeta original o el contenedor. 
  
Las siguientes propiedades que conforman el conjunto en una tabla de jerarquías de columnas necesarias:
  
|||
|:-----|:-----|
|**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** contiene el nombre para el contenedor o la carpeta que debe aparecer en la presentación de la jerarquía. 
  
 **Entrada del objeto** es el identificador de entrada asociado a este contenedor o la carpeta. Se espera un identificador de entrada a largo plazo. Los clientes y MAPI pueden pasar este identificador de entrada a **OpenEntry** para abrir el contenedor o la carpeta y ver su contenido mediante una llamada a [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md). 
  
 **PR_DEPTH** es un valor numérico que indica el nivel de sangría para este contenedor o la carpeta con cero es el nivel superior. Reside el más profunda en la jerarquía de un contenedor o una carpeta, cuanto mayor sea el valor de su propiedad **PR_DEPTH** . Los clientes de usar la propiedad **PR_DEPTH** para mostrar una tabla de jerarquías de forma adecuada para que los usuarios puedan ver claramente relaciones primarias y secundarias. Profundidad de contenedor o la carpeta es siempre en relación con el contenedor o la carpeta de implementación de la tabla de jerarquía. 
  
 **PR_OBJECT_TYPE** siempre se establece en MAPI_ABCONT para tablas de jerarquía de la libreta de direcciones y MAPI_FOLDER para las tablas de jerarquía de carpeta. 
  
 **PR_DISPLAY_TYPE** es un valor numérico que se relaciona con cómo un contenedor o una carpeta se muestra en la tabla de jerarquía. Se utiliza principalmente para fines de presentación, para diferenciar visualmente entre tipos de contenedores o las carpetas. Mensaje muchos almacenar y usar iconos para los tipos de presentación diferentes de proveedores de la libreta de direcciones. Es responsabilidad del proveedor para suministrar estos iconos; MAPI no proporcionar valores predeterminados. 
  
MAPI define muchos valores para **PR_DISPLAY_TYPE**, algunos que son válidos para las carpetas y otras que se usan con las tablas de jerarquía de contenedores de la libreta de direcciones. Normalmente, **PR_DISPLAY_TYPE una carpeta** se establece en DT_FOLDER para indicar un icono de carpeta de forma predeterminada, DT_FOLDER_LINK para indicar un icono que representa un vínculo a otra carpeta o DT_FOLDER_SPECIAL para indicar un icono que es específico de la aplicación. DT_FOLDER_LINK se usa con las carpetas de resultados de búsqueda. 
  
Además de estas columnas obligatorias, tablas de jerarquía de la libreta de direcciones deben incluir la propiedad **PR_CONTAINER_FLAGS** . **PR_CONTAINER_FLAGS** indica diversos atributos acerca de un contenedor en la jerarquía y se usa para distinguir un contenedor de otro. 
  
Una propiedad opcional para tablas de jerarquía de la libreta de direcciones es la propiedad **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)).
  
Tablas de jerarquía del almacén de mensajes incluyan estas propiedades en su conjunto de columna necesarios:
  
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
Los proveedores de la libreta de direcciones deben admitir los siguientes métodos **IMAPITable** en sus implementaciones de la tabla de jerarquía debido a que son necesarios para la libreta de direcciones integrada de MAPI: 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[Tablas MAPI](mapi-tables.md)

