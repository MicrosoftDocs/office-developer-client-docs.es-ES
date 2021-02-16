---
title: Propiedad canónica PidTagFolderAssociatedContents
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderAssociatedContents
api_type:
- HeaderDef
ms.assetid: d1f3f589-dc2d-4538-a13f-278dad29bcc7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c85c5d7c3e80508c4d328f69ac4ad15f0f2c355a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316306"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a>Propiedad canónica PidTagFolderAssociatedContents

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un objeto de tabla de contenido incrustado que proporciona información acerca de la tabla de contenido asociada. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_FOLDER_ASSOCIATED_CONTENTS  <br/> |
|Identificador:  <br/> |0x3610  <br/> |
|Tipo de datos:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Contenedor MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

La tabla de contenido asociada representa una subcarpeta que no aparece en la tabla de contenido estándar. Contiene los mensajes asociados u ocultos de la carpeta. 
  
Esta propiedad puede excluirse en operaciones [IMAPIProp::CopyTo](imapiprop-copyto.md) o incluirse en [operaciones IMAPIProp::CopyProps.](imapiprop-copyprops.md) Como propiedad de **tipo** PT_OBJECT , el método [IMAPIProp::GetProps](imapiprop-getprops.md) no puede recuperarla correctamente; el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) debe tener acceso a su contenido, solicitando el **IID_IMAPITable** de interfaz. Los proveedores de servicios deben notificarlo al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) si está establecido, pero opcionalmente pueden notificarlo o no si no está establecido. 
  
Para recuperar el contenido de la tabla, las aplicaciones cliente deben llamar al [método IMAPIContainer::GetContentsTable.](imapicontainer-getcontentstable.md) Para obtener más información sobre las tablas de contenido de carpetas, vea [Tablas de contenido](contents-tables.md) y Mostrar una tabla de contenido de [carpeta.](displaying-a-folder-contents-table.md) 
  
El **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) y esta propiedad son similares en uso. Varias propiedades MAPI proporcionan acceso a las tablas: 
  
|**Propiedad**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Tabla Contents  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Tabla Jerarquía  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** <br/> |Tabla de contenido asociado  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Tabla Attachment  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Tabla Recipient  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convierte entre IETF RFC2445, RFC2446 y RFC2447, y elementos de citas y reuniones.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedad canónica PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

