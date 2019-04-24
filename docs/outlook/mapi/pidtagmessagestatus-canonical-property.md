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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355723"
---
# <a name="pidtagmessagestatus-canonical-property"></a>Propiedad canónica PidTagMessageStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de 32 bits de marcas que define el estado de un mensaje en una tabla de contenido. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MSG_STATUS  <br/> |
|Identificador:  <br/> |0x0E17  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mensajes generales  <br/> |
   
## <a name="remarks"></a>Comentarios

Puede existir un mensaje en una tabla de contenido y en una o varias tablas de resultados de búsqueda, y cada instancia del mensaje puede tener un estado diferente. Esta propiedad no debe considerarse una propiedad de un mensaje, sino una columna de una tabla de contenido. 
  
Una aplicación cliente puede establecer uno o más de los siguientes indicadores en esta propiedad: 
  
MSGSTATUS_ANSWERED 
  
> Se ha respondido al mensaje. 
    
MSGSTATUS_DELMARKED 
  
> El mensaje se ha marcado para su posterior eliminación. 
    
MSGSTATUS_DRAFT 
  
> El mensaje está en estado de revisión de borrador. 
    
MSGSTATUS_HIDDEN 
  
> El mensaje se debe suprimir de las visualizaciones de carpetas de los destinatarios. 
    
MSGSTATUS_HIGHLIGHTED 
  
> El mensaje se resaltará en la carpeta de muestra de los destinatarios. 
    
MSGSTATUS_REMOTE_DELETE 
  
> El mensaje se marcó para ser eliminado en el almacén de mensajes remoto sin descargarse al cliente local. 
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> El mensaje se marcó para descargar del almacén de mensajes remoto en el cliente local. 
    
MSGSTATUS_TAGGED 
  
> El mensaje se ha etiquetado para un propósito definido por el cliente.
    
El cliente define los indicadores **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**y **MSGSTATUS_TAGGED** . Los proveedores de transporte y almacenamiento pasan estos bits sin ninguna acción. 
  
Los clientes pueden interpretar estos valores de manera que sean apropiados para sus aplicaciones. Una forma por la que muchos clientes usan esta propiedad es mostrar los mensajes marcados para su eliminación con un icono representativo. 
  
Un cliente del visor remoto puede establecer **MSGSTATUS_REMOTE_DELETE** o **MSGSTATUS_REMOTE_DOWNLOAD** en los mensajes de la carpeta de encabezado que el proveedor de transporte remoto presenta a él. La aplicación cliente puede examinar cada encabezado de mensaje en esta carpeta para determinar si el mensaje debe descargarse o eliminarse en el almacén de mensajes remotos. A continuación, se usa el método [IMAPIFolder:: SetMessageStatus](imapifolder-setmessagestatus.md) para establecer la marca adecuada. **SetMessageStatus** es la única forma de establecer cualquiera de las marcas en esta propiedad; no se puede usar el método [IMAPIProp:: SetProps](imapiprop-setprops.md) . Para recuperar esta propiedad, los clientes llaman a [IMAPIFolder:: GetMessageStatus](imapifolder-getmessagestatus.md) en lugar de [IMAPIProp:: GetProps](imapiprop-getprops.md).
  
Los bits 16 a 31 (0x10000 a 0x80000000) de esta propiedad están disponibles para su uso por parte de la aplicación cliente interpersonal de mensajes (IPM). El resto de los bits están reservados para su uso por parte de MAPI; los que no están definidos en la tabla anterior deben establecerse inicialmente en cero y no modificarse posteriormente. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla los datos de objetos de mensajería que se sincronizan entre un servidor y un cliente.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[IMAPITable::QueryRows](imapitable-queryrows.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

