---
title: Propiedad canónica PidTagRtfInSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfInSync
api_type:
- COM
ms.assetid: 443cc68e-7898-4285-a606-f916fcd18554
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ed038faf44f350b041191373cf573e7e185337c7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383061"
---
# <a name="pidtagrtfinsync-canonical-property"></a>Propiedad canónica PidTagRtfInSync

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) tiene el mismo contenido de texto que la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para este mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RTF_IN_SYNC  <br/> |
|Identificador:  <br/> |0x0E1F  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Correo electrónico  <br/> |
   
## <a name="remarks"></a>Comentarios

Un valor de TRUE significa que la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la versión de texto sin formato de este mensaje y la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), la versión de formato de texto enriquecido (RTF), son idénticas, excepto para espacio en blanco en **PR_BODY** y el formato **PR_RTF_COMPRESSED**. El texto en las dos versiones consta de los mismos caracteres en la misma secuencia.
  
Un valor de FALSE significa que las dos versiones no están sincronizadas para el contenido de texto, pero son capaces de que se están sincronizando por la función [RTFSync](rtfsync.md) . Se ha modificado una versión y la otra versión no tiene. 
  
Ningún valor significa que las dos versiones, si ambos existen o nunca existían, no se puede sincronizar. Se ha eliminado o modificado completamente que ya no es posible la sincronización de una versión.
  
Una aplicación cliente que ha modificado **PR_RTF_COMPRESSED** debe establecer el valor FALSE en esta propiedad para forzar la sincronización. Los almacenes de mensajes RTF reconozca deben realizar la sincronización con **RTFSync** durante una llamada de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Los clientes de tener en cuenta RTF deben comprobar la configuración de **PR_RTF_IN_SYNC** antes de leer **PR_RTF_COMPRESSED**y llamar primero a **RTFSync** si es necesario. 
  
Si **PR_BODY** ha tenido modificaciones en un valor distinto de su espacio en blanco, el almacén de mensajes debe eliminar **PR_RTF_IN_SYNC** para finalizar la sincronización. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
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

