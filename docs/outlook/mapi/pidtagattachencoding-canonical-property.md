---
title: Propiedad canónica PidTagAttachEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachEncoding
api_type:
- HeaderDef
ms.assetid: 3b30cec6-da1e-4ef1-8c17-24b66f31cf0a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4bda4783012a3a5cd50d9c0aea6a37ccd238b660
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345496"
---
# <a name="pidtagattachencoding-canonical-property"></a>Propiedad canónica PidTagAttachEncoding

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un identificador de objeto ASN. 1 que especifica la codificación de datos adjuntos. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_ENCODING  <br/> |
|Identificador:  <br/> |0x3702  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad identifica el algoritmo usado para transformar los datos en datos adjuntos.
  
 **Nota:** Las propiedades **PR_ATTACH_ENCODING** y **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) no deben confundirse. No están emparejados ni relacionados. **PR_ATTACH_TAG** identifica la aplicación que generó originalmente los datos adjuntos. "Objeto" tiene un significado mucho más general en el identificador de objeto term y en X. 400, que en la programación orientada a objetos. 
  
La sintaxis del identificador de objeto y los identificadores de objeto de ejemplo se definen en MAPIOID. H archivo de encabezado. Los valores de **PR_ATTACH_ENCODING** no se limitan a los definidos en MAPIOID. H. Por ejemplo, los archivos Macintosh adjuntos pueden usar un identificador como MacBinary. 
  
Para obtener información completa sobre estos identificadores de objeto, consulte la documentación de ASN. 1, X. 208 y X. 209. El identificador de objeto se encuentra en el elemento Application-Reference del entorno de FTBP (parte de cuerpo de transferencia de archivos). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
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

