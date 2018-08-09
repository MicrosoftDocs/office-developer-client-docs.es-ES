---
title: Propiedad canónica PidTagMessageAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageAttachments
api_type:
- HeaderDef
ms.assetid: 85762771-b823-4227-9a7b-75b6ac280b2d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5b76a73a0fde8f4531b99a58646b927724162e81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819713"
---
# <a name="pidtagmessageattachments-canonical-property"></a>Propiedad canónica PidTagMessageAttachments

  
  
**Hace referencia a**: Outlook 
  
Contiene una tabla de las restricciones que se pueden aplicar a una tabla de contenido para buscar todos los mensajes que contienen los subobjetos de datos adjuntos que cumplen las restricciones. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MESSAGE_ATTACHMENTS  <br/> |
|Identificador:  <br/> |0x0E13  <br/> |
|Tipo de datos:  <br/> |PT OBJECT  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad puede ser en las operaciones de [IMAPIProp::CopyTo](imapiprop-copyto.md) incluyen o excluyen de operaciones de [IMAPIProp::CopyProps](imapiprop-copyprops.md) . Como una propiedad de tipo pt Object, no se correctamente puede recuperar mediante el método [IMAPIProp::GetProps](imapiprop-getprops.md) . El método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , que solicita el identificador de interfaz **IID_IMAPITable** debe tener acceso a su contenido. Proveedores de servicios deben identificarlo al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) si se establece, pero es posible que, opcionalmente, identificarlo o no, si no está establecido. 
  
Para recuperar el contenido de la tabla, una aplicación de cliente debe llamar al método de [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) . For more information, see [Tablas de datos adjuntos](attachment-tables.md). 
  
Esta propiedad se puede utilizar para la restricción de subobjetos mediante la especificación de la estructura de [SSubRestriction](ssubrestriction.md) . Esto permite que el cliente limitar la vista de un contenedor para los mensajes con datos adjuntos de la reunión criterios dados. Un mensaje se califica para ver si hay al menos una fila en su tabla de datos adjuntos, es decir, un dato adjunto, satisface la restricción de subobjetos. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)
  
> Define las estructuras de datos básicos que se usan en las operaciones remotas.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define las estructuras de datos básicos que se usan en las operaciones remotas.
    
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

