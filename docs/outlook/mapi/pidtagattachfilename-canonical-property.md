---
title: Propiedad canónica PidTagAttachFilename
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFilename
api_type:
- HeaderDef
ms.assetid: cbf34dd6-7733-47f6-9c41-9d82656ca9dc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f5dcf90e8224f1bf2e96042a7344109293cc2c3f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385714"
---
# <a name="pidtagattachfilename-canonical-property"></a>Propiedad canónica PidTagAttachFilename

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre de archivo base y la extensión, excluyendo la ruta de acceso de datos adjuntos.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W  <br/> |
|Identificador:  <br/> |0x3704  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Se recomienda que los objetos attachment exponen estas propiedades que son aplicables a los valores **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**y **ATTACH_BY_REF_ONLY** de la **PR_ATTACH_METHOD** Propiedad ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)). **PR_ATTACH_FILENAME** y las propiedades asociadas son necesarias cuando se usa alguno de estos valores. 
  
Estas propiedades se pueden usar como un nombre de archivo sugerido para guardar los datos adjuntos y proporcionar la extensión de nombre de archivo si no se proporciona la propiedad **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)). 
  
El nombre de archivo está restringido a ocho caracteres más una extensión de tres caracteres. Para una plataforma que admite nombres de archivo largos, establezca esta propiedad y la propiedad **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)). 
  
MAPI sólo funciona con los nombres de archivo y otras cadenas pasan a ella, en el juego de caracteres estadounidense National Standards Institute (ANSI). Las aplicaciones de cliente que usan nombres de archivo en un juego de caracteres del fabricante de equipos originales (OEM) deben convertirlos a ANSI antes de llamar a MAPI. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Especifica las propiedades de mensajes codificados con derechos administrados.
    
[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)
  
> Especifica S/MIME firmados y cifrados de propiedades del mensaje.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.
    
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

