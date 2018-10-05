---
title: Propiedad canónica PidTagMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageStatus
api_type:
- HeaderDef
ms.assetid: e479e863-a8de-4f7e-9eae-3f721cd16e9a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dacd759d978394a5f4ed028915ed1c717bf6efe5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382809"
---
# <a name="pidtagmessagestatus-canonical-property"></a>Propiedad canónica PidTagMessageStatus

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits 32 bits de indicadores que define el estado de un mensaje en una tabla de contenido. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MSG_STATUS  <br/> |
|Identificador:  <br/> |0x0E17  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

Puede haber un mensaje en una tabla de contenido y en una o varias tablas de resultados de búsqueda, y cada instancia del mensaje puede tener un estado diferente. Esta propiedad no se debe considerar una propiedad en un mensaje, pero una columna de una tabla de contenido. 
  
Una aplicación cliente puede establecer una o varias de las siguientes marcas en esta propiedad: 
  
MSGSTATUS_ANSWERED 
  
> El mensaje se ha respondido. 
    
MSGSTATUS_DELMARKED 
  
> El mensaje se ha marcado para su eliminación subsiguiente. 
    
MSGSTATUS_DRAFT 
  
> El mensaje está en estado de revisión de borrador. 
    
MSGSTATUS_HIDDEN 
  
> El mensaje es se suprimen de muestra de la carpeta de los destinatarios. 
    
MSGSTATUS_HIGHLIGHTED 
  
> El mensaje es se resalta en la muestra de la carpeta de los destinatarios. 
    
MSGSTATUS_REMOTE_DELETE 
  
> El mensaje se ha marcado para su eliminación en el almacén de mensajes remoto sin descargar en el cliente local. 
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> El mensaje se ha marcado para la descarga desde el almacén de mensajes remoto para el cliente local. 
    
MSGSTATUS_TAGGED 
  
> El mensaje se ha etiquetado con un fin definidas por el cliente.
    
Los indicadores **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**y **MSGSTATUS_TAGGED** se definen por el cliente. Proveedores de transporte y almacén de pasan estos bits sin ninguna acción. 
  
Los clientes pueden interpretar estos valores de cualquier forma que es adecuado para sus aplicaciones. Es una forma de que muchos clientes usan esta propiedad Mostrar los mensajes marcados para eliminación con un icono representativo. 
  
Un cliente remoto Visor puede establecer **MSGSTATUS_REMOTE_DELETE** o **MSGSTATUS_REMOTE_DOWNLOAD** en los mensajes en la carpeta de encabezado presentada por el proveedor de transporte remoto. La aplicación cliente puede examinar cada encabezado de mensaje en esta carpeta para determinar si el mensaje debe ser descargado o eliminado en el almacén de mensajes remoto. A continuación, se usa el método [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) para establecer la marca adecuada. **SetMessageStatus** es la única forma de establecer cualquiera de los indicadores de esta propiedad; no se puede usar el método [IMAPIProp::SetProps](imapiprop-setprops.md) . Para recuperar esta propiedad, los clientes llaman [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) en lugar de [IMAPIProp::GetProps](imapiprop-getprops.md).
  
Bits 16 a 31 (0 x 10000 a través de 0 x 80000000) de esta propiedad están disponibles para su uso por la aplicación de cliente de mensajes interpersonales (IPM). Todos los demás bits están reservados para su uso por MAPI; los no definidos en la tabla anterior deben inicialmente se establece en cero y no modifica posteriormente. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla la sincronización de datos de objeto mensajería entre un servidor y un cliente.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[IMAPITable::QueryRows](imapitable-queryrows.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

