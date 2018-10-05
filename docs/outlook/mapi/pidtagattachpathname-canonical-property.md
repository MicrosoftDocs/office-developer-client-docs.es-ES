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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389172"
---
# <a name="pidtagattachpathname-canonical-property"></a>Propiedad canónica PidTagAttachPathname

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene la ruta de acceso completa y el nombre de archivo de datos adjuntos.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W  <br/> |
|Identificador:  <br/> |0x3708  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Se recomienda que los datos adjuntos subobjetos exponen estas propiedades. Establecerlas indica que los datos adjuntos no se incluye con el mensaje, pero está disponibles en un servidor de archivos comunes. Estas propiedades son necesarias en combinación con cualquiera de las marcas de **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) que indican datos adjuntos por referencia: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**o **ATTACH_BY_REF_ SÓLO**. 
  
Cada nombre de archivo o directorio está restringida a un nombre de ocho caracteres más una extensión de tres caracteres. La ruta de acceso global está restringido a 256 caracteres. Para una plataforma que admite nombres de archivo largos, establecer estas propiedades y la **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)). 
  
Aplicaciones cliente deben usar una convención de nomenclatura universal (UNC) en la mayoría de los casos, cuando el archivo se comparte y debe usar una ruta de acceso absoluta cuando el archivo es local.
  
MAPI sólo funciona con las rutas de acceso y conjunto de caracteres de los nombres de archivo en el ANSI. Los clientes que usan nombres de archivo y rutas de acceso en un juego de caracteres OEM deben convertirlos a ANSI antes de llamar a MAPI. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Especifica las propiedades de mensajes codificados con derechos administrados.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[ScLocalPathFromUNC](sclocalpathfromunc.md)
  
[ScUNCFromLocalPath](scuncfromlocalpath.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

