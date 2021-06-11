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
ms.openlocfilehash: 5a908b3543dff5cf011c9bd4d5d05b3a07004ead
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361085"
---
# <a name="pidtagattachtag-canonical-property"></a>Propiedad canónica PidTagAttachTag

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un identificador de objeto ASN.1 que especifica la aplicación que proporcionó datos adjuntos. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_TAG  <br/> |
|Identificador:  <br/> |0x370A  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad identifica la aplicación que generó originalmente los datos adjuntos.
  
 **Nota** Las **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) y **PR_ATTACH_TAG** propiedades no deben confundirse. No están emparejados ni relacionados. **PR_ATTACH_ENCODING** identifica el algoritmo usado para transformar los datos de un archivo adjunto. "Object" tiene un significado mucho más general en el identificador de objeto de término, y en el uso de X.400, que en la programación orientada a objetos. 
  
La sintaxis del identificador de objeto y los identificadores de objeto de ejemplo se definen en MAPIOID. Archivo de encabezado H. Los valores **PR_ATTACH_TAG** no se limitan a los definidos en MAPIOID.H. 
  
Para obtener información completa sobre estos identificadores de objeto, consulte la documentación de ASN.1, X.208 y X.209. El identificador de objeto se encuentra en el elemento de referencia de la aplicación del entorno de la parte del cuerpo de transferencia de archivos (FTBP). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

