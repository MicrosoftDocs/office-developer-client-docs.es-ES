---
title: Propiedad canónica PidTagContainerContents
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerContents
api_type:
- HeaderDef
ms.assetid: 66dbe65a-b9fd-41d5-946f-ec8888363043
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5f0717c2a6def6f99f1e53217764e8820125b79d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283131"
---
# <a name="pidtagcontainercontents-canonical-property"></a>Propiedad canónica PidTagContainerContents

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un objeto de tabla de contenido incrustado que proporciona información acerca de un contenedor.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTAINER_CONTENTS  <br/> |
|Identificador:  <br/> |0x360F  <br/> |
|Tipo de datos:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad puede excluirse en operaciones [IMAPIProp::CopyTo](imapiprop-copyto.md) o incluirse en [operaciones IMAPIProp::CopyProps.](imapiprop-copyprops.md) Como propiedad de tipo PT_OBJECT, el método [IMAPIProp::GetProps](imapiprop-getprops.md) no puede recuperarla correctamente; el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) debe tener acceso a su contenido, solicitando el IID_IMAPITable de interfaz. Los proveedores de servicios deben notificarlo al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) si está establecido, pero opcionalmente pueden notificarlo o no si no está establecido. 
  
Para recuperar el contenido de la tabla, una aplicación cliente debe llamar al método [IMAPIContainer::GetContentsTable.](imapicontainer-getcontentstable.md) For more information, see [Tablas de contenido](contents-tables.md). 
  
Esta propiedad, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) y **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) son similares en uso. Varias propiedades MAPI proporcionan acceso a las tablas: 
  
|**Propiedad**|**Table**|
|:-----|:-----|
|PidTagContainerContents  <br/> |Tabla Contents  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Tabla Hierarchy  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Tabla de contenido asociado  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Tabla Attachment  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Tabla Recipient  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

