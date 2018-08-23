---
title: Propiedad canónica PidTagAttachSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachSize
api_type:
- HeaderDef
ms.assetid: 768b3215-dd9f-4aa0-b52c-178ca81a7b07
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fd98044868bbec36ed14fcf90deb2990039244b8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573743"
---
# <a name="pidtagattachsize-canonical-property"></a>Propiedad canónica PidTagAttachSize

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la suma, en bytes, de los tamaños de todas las propiedades en un archivo adjunto. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_SIZE  <br/> |
|Identificador:  <br/> |0x0E20  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Se recomienda que los datos adjuntos subobjetos exponen la propiedad **PR_ATTACH_SIZE** . La suma contenida en **PR_ATTACH_SIZE** incluye el tamaño de la propiedad de **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) o **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)). Por lo tanto, **PR_ATTACH_SIZE** es suelen ser mayores que el contenido de los datos adjuntos por sí solo. 
  
Esta propiedad se puede usar para comprobar el tamaño aproximado de los datos adjuntos antes de realizar a una transferencia remota por módem y para mostrar los indicadores de progreso al guardar los datos adjuntos en el disco. Es especialmente útil con objetos OLE adjuntos. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedad canónica PidTagMessageSize](pidtagmessagesize-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

