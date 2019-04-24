---
title: Propiedad canónica PidTagMessageRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipients
api_type:
- HeaderDef
ms.assetid: 7f8b0d96-99d6-4f1c-8ac4-4dbb83626382
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d30088ba7398669228a18be825323afa800ec536
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355688"
---
# <a name="pidtagmessagerecipients-canonical-property"></a>Propiedad canónica PidTagMessageRecipients

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una tabla de restricciones que se pueden aplicar a una tabla de contenido para buscar todos los mensajes que contienen subobjetos de destinatarios que cumplen con las restricciones. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MESSAGE_RECIPIENTS  <br/> |
|Identificador:  <br/> |0x0E12  <br/> |
|Tipo de datos:  <br/> |PT OBJECT  <br/> |
|Área:  <br/> |Mensajes generales  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se puede excluir en las operaciones de [IMAPIProp:: CopyTo](imapiprop-copyto.md) o incluirse en las operaciones de [IMAPIProp:: CopyProps](imapiprop-copyprops.md) . Como una propiedad de tipo **PT Object**, el método [IMAPIProp:: GetProps](imapiprop-getprops.md) no puede recuperarlo correctamente. Debe obtener acceso a su contenido mediante el método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , lo que solicita el identificador de interfaz **IID_IMAPITable** . Los proveedores de servicios deben informar al método [IMAPIProp:: GetPropList](imapiprop-getproplist.md) si está establecido, pero, opcionalmente, puede informar de él o no si no se ha establecido. 
  
Para recuperar el contenido de la tabla, una aplicación cliente debe llamar al método [IMessage:: GetRecipientTable](imessage-getrecipienttable.md) . 
  
Esta propiedad se puede usar para la restricción de subobjeto al especificarla en la estructura [SSubRestriction](ssubrestriction.md) . Esto permite a un cliente limitar la vista de un contenedor a los mensajes con los destinatarios que cumplen los criterios especificados. Un mensaje es apto para ver si al menos una fila de su tabla de destinatarios, es decir, un destinatario satisface la restricción de subobjeto. 
  
 **Nota:** El uso de resultados de restricción de subobjeto es el equivalente de una llamada de [IMAPISession:: OpenEntry](imapisession-openentry.md) en todos los mensajes de la tabla. Según la aplicación cliente y el número de mensajes que se va a buscar, puede afectar al rendimiento. 
  
La propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) y esta propiedad son de uso similar. Varias propiedades MAPI proporcionan acceso a las tablas: 
  
|**Property**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Tabla contenido  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Tabla de jerarquía  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Tabla de contenido asociada  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Tabla de datos adJuntos  <br/> |
|PR_MESSAGE_RECIPIENTS  <br/> |Tabla de destinatarios  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla el orden y el flujo de transferencias de datos entre un cliente y un servidor.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Habilita el control de las listas de permitidos y bloqueados y la determinación de los mensajes de correo electrónico no deseado.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficaz.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

