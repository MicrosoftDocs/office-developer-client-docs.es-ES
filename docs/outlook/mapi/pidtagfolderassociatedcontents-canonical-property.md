---
title: Propiedad canónico PidTagFolderAssociatedContents
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: fe6395029e312a19bce6252e73b4616bb0aa0851
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819504"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a>Propiedad canónico PidTagFolderAssociatedContents

  
  
**Se aplica a**: Outlook 
  
Contiene un objeto de tabla de contenido incrustado que proporciona información acerca de la tabla de contenido asociada. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_FOLDER_ASSOCIATED_CONTENTS  <br/> |
|Identificador:  <br/> |0x3610  <br/> |
|Tipo de datos:  <br/> |PT OBJECT  <br/> |
|Área:  <br/> |Contenedor MAPI  <br/> |
   
## <a name="remarks"></a>Notas

En la tabla de contenido asociada representa una subcarpeta que no aparecen en la tabla de contenido estándar. Contiene los mensajes asociado u ocultas, de la carpeta. 
  
Esta propiedad puede ser en las operaciones de [IMAPIProp::CopyTo](imapiprop-copyto.md) incluyen o excluyen de operaciones de [IMAPIProp::CopyProps](imapiprop-copyprops.md) . Como una propiedad de tipo **pt Object**, no se correctamente puede recuperar mediante el método [IMAPIProp::GetProps](imapiprop-getprops.md) ; el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , que solicita el identificador de interfaz **IID_IMAPITable** debe tener acceso a su contenido. Proveedores de servicios deben identificarlo al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) si se establece, pero es posible que, opcionalmente, identificarlo o no, si no está establecido. 
  
Para recuperar el contenido de la tabla, las aplicaciones cliente deben llamar al método de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) . Para obtener más información sobre las tablas de contenido de carpeta, vea [Las tablas de contenido](contents-tables.md) y [Mostrar una tabla de contenido de carpeta](displaying-a-folder-contents-table.md). 
  
**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) y esta propiedad son similares en uso. Varias propiedades MAPI proporcionan acceso a las tablas: 
  
|**Propiedad**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Tabla de contenido  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Tabla de jerarquía  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** <br/> |Tabla de contenido asociada  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Tabla de datos adjuntos  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Tabla de destinatarios  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y elementos de reunión.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Ver también



[Propiedad canónico PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

