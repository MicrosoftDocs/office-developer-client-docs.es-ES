---
title: Propiedad canónica PidTagContentCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCount
api_type:
- HeaderDef
ms.assetid: 27c75031-a968-4636-98a6-4a5b7422f57c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7e9994da72bbc38a546f220e5ecf8768b80c6f1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331958"
---
# <a name="pidtagcontentcount-canonical-property"></a>Propiedad canónica PidTagContentCount

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el número de mensajes de una carpeta, calculado por el almacén de mensajes.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTENT_COUNT  <br/> |
|Identificador:  <br/> |0x3602  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad calculada por el almacén de mensajes se usa para dos propósitos diferentes, aunque relacionados. En un objeto MapiFolder, contiene el número de mensajes de una carpeta. En una fila de título en tablas MAPI categorizadas, contiene el número de mensajes no asociados en la categoría correspondiente a esa fila de título.
  
El número contenido en esta propiedad no incluye entradas asociadas en la carpeta. **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contiene el recuento de mensajes no leídos de la carpeta. Una aplicación cliente puede leer pero no cambiar esta propiedad y **PR_CONTENT_UNREAD**. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Microsoft Exchange Server protocolo relacionados.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Controla las operaciones de carpeta.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Incluye operaciones permitidas para los objetos de tabla principales.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

