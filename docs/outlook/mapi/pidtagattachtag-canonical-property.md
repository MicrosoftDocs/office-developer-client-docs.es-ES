---
title: Propiedad canónica PidTagAttachTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTag
api_type:
- HeaderDef
ms.assetid: 3d223809-b697-47c6-bc3c-2206aff7ad33
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: af5d05ee6d3592694952002c16e16188c3e458a4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565623"
---
# <a name="pidtagattachtag-canonical-property"></a>Propiedad canónica PidTagAttachTag

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un identificador de objeto ASN.1 que especifica la aplicación que suministró un dato adjunto. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_TAG  <br/> |
|Identificador:  <br/> |0x370A  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad identifica la aplicación que generó originalmente los datos adjuntos.
  
 **Nota** No se deben confundir las propiedades **PR_ATTACH_TAG** y **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)). No están emparejados o relacionados con. **PR_ATTACH_ENCODING** identifica el algoritmo utilizado para transformar los datos en un archivo adjunto. "Objeto" tiene un significado mucho más general en el identificador de objeto de términos y en el uso X.400, que en la programación orientada a objetos. 
  
Los identificadores de objeto de ejemplo y sintaxis de identificador de objeto se definen en el MAPIOID. Archivo de encabezado H. Los valores de **PR_ATTACH_TAG** no se limitan a los definidos en MAPIOID. H. 
  
Para obtener información detallada sobre estos identificadores de objetos, vea la documentación en ASN.1, X.208 y X.209. El identificador de objeto se encuentra en el elemento de referencia de la aplicación del entorno de parte de cuerpo de transferencia de archivo (FTBP). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedad canónica PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

