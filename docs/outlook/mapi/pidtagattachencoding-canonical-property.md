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
ms.openlocfilehash: cdeb432e20f2779bbb625566108551748b48a01f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819234"
---
# <a name="pidtagattachencoding-canonical-property"></a>Propiedad canónica PidTagAttachEncoding

  
  
**Hace referencia a**: Outlook 
  
Contiene un identificador de objeto ASN.1 que especifica la codificación de los datos adjuntos. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_ENCODING  <br/> |
|Identificador:  <br/> |0x3702  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad identifica el algoritmo utilizado para transformar los datos en un archivo adjunto.
  
 **Nota** No se deben confundir el **PR_ATTACH_ENCODING** y las propiedades de **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). No están emparejados o relacionados con. **PR_ATTACH_TAG** identifica la aplicación que generó originalmente los datos adjuntos. "Objeto" tiene un significado mucho más general en el identificador de objeto de términos y en X.400, que en la programación orientada a objetos. 
  
Los identificadores de objeto de ejemplo y sintaxis de identificador de objeto se definen en el MAPIOID. Archivo de encabezado H. Los valores de **PR_ATTACH_ENCODING** no se limitan a los definidos en MAPIOID. H. Por ejemplo, archivos de Macintosh adjuntos pueden usar un identificador como MacBinary. 
  
Para obtener información detallada sobre estos identificadores de objetos, vea la documentación en ASN.1, X.208 y X.209. El identificador de objeto se encuentra en el elemento de referencia de la aplicación del entorno FTBP (elementos de cuerpo de transferencia de archivo). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
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

