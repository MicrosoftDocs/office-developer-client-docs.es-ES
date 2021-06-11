---
title: Propiedad canónica PidTagContainerHierarchy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerHierarchy
api_type:
- HeaderDef
ms.assetid: 6917510d-ca1e-4049-9eab-09313753ecf0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f009d7ce5cd1856ccff1e00953188c8edde7a6bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332861"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a>Propiedad canónica PidTagContainerHierarchy

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un objeto de tabla de jerarquía incrustada que proporciona información sobre los contenedores secundarios. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTAINER_HIERARCHY  <br/> |
|Identificador:  <br/> |0x360E  <br/> |
|Tipo de datos:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad puede excluirse en operaciones [IMAPIProp::CopyTo](imapiprop-copyto.md) o incluirse en [operaciones IMAPIProp::CopyProps.](imapiprop-copyprops.md) Como una propiedad de tipo **PT_OBJECT**, el método [IMAPIProp::GetProps](imapiprop-getprops.md) no puede recuperarla correctamente; el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) debe tener acceso a su contenido, solicitando el IID_IMAPITable de interfaz. Los proveedores de servicios deben notificarlo al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) si está establecido, pero opcionalmente pueden notificarlo o no si no está establecido. 
  
Para recuperar el contenido de la tabla, una aplicación cliente debe llamar al método [IMAPIContainer::GetHierarchyTable.](imapicontainer-gethierarchytable.md) Para obtener más información, vea [Hierarchy Tables](hierarchy-tables.md). 
  
 **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) y esta propiedad es similar en uso. Varias propiedades MAPI proporcionan acceso a tablas: 
  
|**Property**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Tabla contenido  <br/> |
|**PR_CONTAINER_HIERARCHY** <br/> |Tabla jerarquía  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Tabla de contenido asociada  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Tabla de datos adjuntos  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Tabla de destinatarios  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

