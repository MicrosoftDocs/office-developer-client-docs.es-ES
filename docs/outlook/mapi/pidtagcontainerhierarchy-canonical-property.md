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
ms.openlocfilehash: 691c5977092b5e2ca6b453209982dd1333a6df89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819359"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a>Propiedad canónica PidTagContainerHierarchy

  
  
**Hace referencia a**: Outlook 
  
Contiene un objeto de la tabla de jerarquía incrustado que proporciona información sobre el elemento secundario de contenedores. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTAINER_HIERARCHY  <br/> |
|Identificador:  <br/> |0x360E  <br/> |
|Tipo de datos:  <br/> |PT OBJECT  <br/> |
|Área:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad puede ser en las operaciones de [IMAPIProp::CopyTo](imapiprop-copyto.md) incluyen o excluyen de operaciones de [IMAPIProp::CopyProps](imapiprop-copyprops.md) . Como una propiedad de tipo **pt Object**, no se correctamente puede recuperar mediante el método [IMAPIProp::GetProps](imapiprop-getprops.md) ; el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , que solicita el identificador de interfaz IID_IMAPITable debe tener acceso a su contenido. Proveedores de servicios deben identificarlo al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) si está establecida, pero puede, opcionalmente, identificarlo o no, si no está establecido. 
  
Para recuperar el contenido de la tabla, una aplicación de cliente debe llamar al método de [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) . Para obtener más información, vea [Las tablas de jerarquía](hierarchy-tables.md). 
  
 **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) y esta propiedad son similares en uso. Varias propiedades MAPI proporcionan acceso a las tablas: 
  
|**Propiedad**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Tabla de contenido  <br/> |
|**PR_CONTAINER_HIERARCHY** <br/> |Tabla de jerarquía  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Tabla de contenido asociada  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Tabla de datos adjuntos  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Tabla de destinatarios  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

