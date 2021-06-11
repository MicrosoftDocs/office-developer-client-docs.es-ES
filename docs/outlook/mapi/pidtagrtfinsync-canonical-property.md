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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357879"
---
# <a name="pidtagrtfinsync-canonical-property"></a>Propiedad canónica PidTagRtfInSync

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si la **propiedad PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) tiene el mismo contenido de texto que la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para este mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RTF_IN_SYNC  <br/> |
|Identificador:  <br/> |0x0E1F  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Correo electrónico  <br/> |
   
## <a name="remarks"></a>Comentarios

Un valor true significa que la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) , la versión de texto sin formato de este mensaje y la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) , la versión de formato de texto enriquecido (RTF), son idénticas excepto para los espacios en blanco en **PR_BODY** y el formato **en PR_RTF_COMPRESSED**. El texto de las dos versiones consta de los mismos caracteres de la misma secuencia.
  
Un valor de FALSE significa que las dos versiones no están sincronizadas para el contenido de texto, pero pueden sincronizarse con la [función RTFSync.](rtfsync.md) Una versión se ha modificado y la otra no. 
  
Ningún valor significa que las dos versiones, si existen o existieron alguna vez, no se pueden sincronizar. Una versión se ha eliminado o modificado de forma tan radical que la sincronización ya no es posible.
  
Una aplicación cliente que haya modificado **PR_RTF_COMPRESSED** debe establecer un valor de FALSE en esta propiedad para forzar la sincronización. Los almacenes de mensajes compatible con RTF deben realizar la sincronización con **RTFSync** durante una [llamada IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Los clientes con rtf deben comprobar la configuración de **PR_RTF_IN_SYNC** antes de **leer PR_RTF_COMPRESSED** y llamar primero **a RTFSync** si es necesario. 
  
Si **PR_BODY** ha tenido modificaciones en cualquier cosa que no sea su espacio en blanco, el almacén de mensajes debe eliminar **PR_RTF_IN_SYNC** para finalizar la sincronización. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
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

