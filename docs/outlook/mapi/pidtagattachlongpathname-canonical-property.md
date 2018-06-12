---
title: Propiedad canónico PidTagAttachLongPathname
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongPathname
api_type:
- HeaderDef
ms.assetid: 3262cf95-48b5-4764-a96e-d752ce35b2dc
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: a2230f2c2b1d4793c425694f76bb79fb7284c479
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819219"
---
# <a name="pidtagattachlongpathname-canonical-property"></a>Propiedad canónico PidTagAttachLongPathname

  
  
**Se aplica a**: Outlook 
  
Contiene la ruta de acceso larga completo y nombre de archivo de un documento adjunto. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W  <br/> |
|Identificador:  <br/> |0x370D  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Notas

Estas propiedades son aplicables cuando se usa alguno de los valores de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) que indican datos adjuntos por referencia: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**o **ATTACH_BY _REF_ONLY**. Plataformas compatibles con nombres de archivo largos deben establecer **PR_ATTACH_LONG_PATHNAME** o propiedades asociadas y las propiedades de **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) cuando se envía y debe comprobar **PR_ATTACH_LONG_PATHNAME **o asociados propiedades primero al recibir. 
  
La aplicación cliente debe establecer estas propiedades en una ruta de acceso sugerida largo y nombre de archivo que se usará si el equipo host de recibir un mensaje admite nombres de archivo largos. Establecer estas propiedades indica que los datos adjuntos no se incluye con el mensaje, pero está disponibles en un servidor de archivos comunes. 
  
A diferencia de los directorios y los nombres de archivo proporcionada por **PR_ATTACH_PATHNAME**, estos directorios y los nombres de archivo no están restringidos en una extensión de tres caracteres además de nombre de archivo o directorio de ocho caracteres. En su lugar, cada nombre de archivo o directorio puede ser hasta 256 caracteres long, incluidos el nombre, la extensión y el período de separador. Sin embargo, la ruta de acceso global está limitado a 256 caracteres. 
  
Los clientes deben usar una convención de nomenclatura universal (UNC) en la mayoría de los casos cuando el archivo se comparte y debe usar una ruta de acceso absoluta cuando el archivo es local.
  
MAPI sólo funciona con las rutas de acceso y conjunto de caracteres de los nombres de archivo en el ANSI. Las aplicaciones de cliente que usan nombres de archivo y rutas de acceso en un juego de caracteres OEM deben convertirlos a ANSI antes de llamar a MAPI. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Especifica las propiedades de mensajes codificados con derechos administrados.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

