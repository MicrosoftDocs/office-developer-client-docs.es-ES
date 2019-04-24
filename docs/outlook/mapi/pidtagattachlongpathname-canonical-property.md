---
title: Propiedad canónica PidTagAttachLongPathname
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d8fe8525cf4fc11ac17ed6d73fb5d97e4f2d003e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339371"
---
# <a name="pidtagattachlongpathname-canonical-property"></a>Propiedad canónica PidTagAttachLongPathname

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre de archivo y la ruta de acceso completos completos de un archivo de datos adjuntos. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W  <br/> |
|Identificador:  <br/> |0x370D  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades se aplican cuando se usa cualquiera de los valores de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) que indican datos adjuntos por referencia: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**o **ATTACH_BY _REF_ONLY**. Las plataformas que admiten nombres de archivo largos deben establecer las propiedades **PR_ATTACH_LONG_PATHNAME** o asociadas y **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) al enviar y deben comprobar **PR_ATTACH_LONG_PATHNAME **o las propiedades asociadas en primer lugar al recibir. 
  
La aplicación cliente debe establecer estas propiedades en una ruta de acceso larga y un nombre de archivo sugeridos que se usarán si el equipo host que recibe un mensaje admite nombres de archivo largos. La configuración de estas propiedades indica que los datos adjuntos no se incluyen en el mensaje, pero que están disponibles en un servidor de archivos común. 
  
A diferencia de los directorios y los nombres de archivo proporcionados por **PR_ATTACH_PATHNAME**, estos directorios y nombres de archivo no están restringidos a un directorio de ocho caracteres o un nombre de archivo más una extensión de tres caracteres. En su lugar, cada directorio o nombre de archivo puede tener hasta 256 caracteres, como el nombre, la extensión y el período separador. Sin embargo, la ruta de acceso general está limitada a 256 caracteres. 
  
Los clientes deben usar una Convención de nomenclatura universal (UNC) en la mayoría de los casos cuando se comparte el archivo y deben usar una ruta de acceso absoluta cuando el archivo es local.
  
MAPI solo funciona con los nombres de archivo y las rutas del juego de caracteres ANSI. Las aplicaciones cliente que usan rutas de acceso y nombres de archivo en un conjunto de caracteres OEM deben convertirlas a ANSI antes de llamar a MAPI. 
  
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



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

