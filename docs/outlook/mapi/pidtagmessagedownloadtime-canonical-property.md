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
ms.openlocfilehash: 8078d31af497a437c983da7447a0aebbdfb643fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325679"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a>Propiedad canónica PidTagMessageDownloadTime

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el tiempo estimado para descargar un mensaje desde un servidor remoto a un almacén de mensajes local. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MESSAGE_DOWNLOAD_TIME  <br/> |
|Identificador:  <br/> |0x0E18  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mensajes generales  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se expresa en segundos y representa la mejor estimación del tiempo que tardaría un proveedor de transporte remoto en descargar un mensaje determinado desde su ubicación actual a un almacén de mensajes local hasta que el cliente vea la carpeta de encabezado. El proveedor de transporte remoto normalmente calcula el valor de esta propiedad dividiendo el valor de la propiedad **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) por la velocidad del vínculo de comunicaciones en bytes por segundo. Si el proveedor no puede calcular el tiempo de descarga, por ejemplo, si no conoce la velocidad del vínculo, debe proporcionar un valor **PT_ERROR** como **MAPI_E_NO_SUPPORT** para esta columna en la tabla contenido de la carpeta de encabezado. 
  
## <a name="related-resources"></a>Recursos relacionados

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

