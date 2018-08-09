---
title: Propiedad canónica PidTagMessageDownloadTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDownloadTime
api_type:
- HeaderDef
ms.assetid: f0d34dd6-7ddb-4843-b848-c89923ff80cc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b47d104ade6a7d23f5630d15697b330360d027b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819734"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a>Propiedad canónica PidTagMessageDownloadTime

  
  
**Hace referencia a**: Outlook 
  
Contiene el tiempo estimado para descargar un mensaje desde un servidor remoto en un almacén de mensajes local. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MESSAGE_DOWNLOAD_TIME  <br/> |
|Identificador:  <br/> |0x0E18  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se expresa en segundos y representa la mejor estimación del tiempo que tardaría un proveedor de transporte remoto para descargar un mensaje determinado desde su ubicación actual en un almacén de mensajes local en el cliente de visualización de la carpeta de encabezado. Normalmente, el proveedor de transporte remoto calcula el valor de esta propiedad dividiendo el valor de la propiedad **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) por la velocidad del vínculo de comunicaciones en bytes por segundo. Si el proveedor no puede calcular el tiempo de descarga, por ejemplo, si no sabe la velocidad del vínculo, debe proporcionar un valor **PT_ERROR** como **MAPI_E_NO_SUPPORT** para esta columna en la tabla de contenido de carpeta de encabezado. 
  
## <a name="related-resources"></a>Recursos relacionados

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

