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
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

Un mensaje puede existir en una tabla de contenido y en una o más tablas de resultados de búsqueda, y cada instancia del mensaje puede tener un estado diferente. Esta propiedad no debe considerarse una propiedad de un mensaje, sino una columna de una tabla de contenido. 
  
Una aplicación cliente puede establecer una o varias de las siguientes marcas en esta propiedad: 
  
MSGSTATUS_ANSWERED 
  
> Se ha respondido al mensaje. 
    
MSGSTATUS_DELMARKED 
  
> El mensaje se ha marcado para su eliminación posterior. 
    
MSGSTATUS_DRAFT 
  
> El mensaje está en estado de borrador de revisión. 
    
MSGSTATUS_HIDDEN 
  
> El mensaje se suprimirá de las pantallas de carpeta de los destinatarios. 
    
MSGSTATUS_HIGHLIGHTED 
  
> El mensaje debe resaltarse en las pantallas de la carpeta de los destinatarios. 
    
MSGSTATUS_REMOTE_DELETE 
  
> El mensaje se ha marcado para su eliminación en el almacén de mensajes remoto sin descargarlo en el cliente local. 
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> El mensaje se ha marcado para su descarga desde el almacén de mensajes remoto al cliente local. 
    
MSGSTATUS_TAGGED 
  
> El mensaje se ha etiquetado para un propósito definido por el cliente.
    
El **cliente MSGSTATUS_DELMARKED,** **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED** y **MSGSTATUS_TAGGED** marca. Los proveedores de transporte y almacenamiento pasan estos bits sin ninguna acción. 
  
Los clientes pueden interpretar estos valores de cualquier forma que sea adecuada para sus aplicaciones. Una forma en que muchos clientes usan esta propiedad es mostrar los mensajes marcados para su eliminación con un icono representativo. 
  
Un cliente de visor remoto puede MSGSTATUS_REMOTE_DELETE **o** **MSGSTATUS_REMOTE_DOWNLOAD** en los mensajes de la carpeta de encabezado que le presenta el proveedor de transporte remoto. La aplicación cliente puede examinar cada encabezado de mensaje de esta carpeta para determinar si el mensaje debe descargarse o eliminarse en el almacén de mensajes remoto. A continuación, usa [el método IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) para establecer la marca adecuada. **SetMessageStatus** es la única forma de establecer cualquiera de las marcas de esta propiedad; No [se puede usar el método IMAPIProp::SetProps.](imapiprop-setprops.md) Para recuperar esta propiedad, los clientes llaman [a IMAPIFolder::GetMessageStatus en](imapifolder-getmessagestatus.md) lugar de [IMAPIProp::GetProps](imapiprop-getprops.md).
  
Los bits del 16 al 31 (0x10000 a 0x80000000) de esta propiedad están disponibles para que los use la aplicación cliente de mensajes interpersonales (IPM). Todos los demás bits están reservados para su uso por MAPI; los que no se definen en la tabla anterior deben establecerse inicialmente en cero y no modificarse posteriormente. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla la sincronización de datos de objetos de mensajería entre un servidor y un cliente.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[IMAPITable::QueryRows](imapitable-queryrows.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

