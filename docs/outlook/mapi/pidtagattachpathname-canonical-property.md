---
title: Propiedad canónica PidTagAttachPathname
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPathname
api_type:
- HeaderDef
ms.assetid: e19c7cd1-7c56-4f63-8736-d6971c7c5f4d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 05df7fe04f511de9310edc7a8ef09130e6354ad2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327233"
---
# <a name="pidtagattachpathname-canonical-property"></a>Propiedad canónica PidTagAttachPathname

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la ruta de acceso completa y el nombre de archivo de un archivo adjunto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W  <br/> |
|Identificador:  <br/> |0x3708  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Se recomienda que los subobjetos de datos adjuntos expongan estas propiedades. Si se establecen, indica que los datos adjuntos no se incluyen en el mensaje, pero que están disponibles en un servidor de archivos común. Estas propiedades son necesarias junto con cualquiera de los indicadores **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) que indican datos adjuntos por referencia: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**o **ATTACH_BY_REF_ SOLO**. 
  
Cada directorio o nombre de archivo está restringido a un nombre de ocho caracteres más una extensión de tres caracteres. La ruta de acceso general está restringida a 256 caracteres. Para una plataforma que admite nombres de archivo largos, establezca estas propiedades y **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)). 
  
Las aplicaciones cliente deben usar una Convención de nomenclatura universal (UNC) en la mayoría de los casos cuando se comparte el archivo y deben usar una ruta de acceso absoluta cuando el archivo es local.
  
MAPI solo funciona con los nombres de archivo y las rutas del juego de caracteres ANSI. Los clientes que usan rutas de acceso y nombres de archivo en un conjunto de caracteres OEM deben convertirlos a ANSI antes de llamar a MAPI. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Especifica las propiedades de los mensajes codificados con derechos administrados.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[ScLocalPathFromUNC](sclocalpathfromunc.md)
  
[ScUNCFromLocalPath](scuncfromlocalpath.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

