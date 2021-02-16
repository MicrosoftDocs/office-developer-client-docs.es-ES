---
title: Propiedad canónica PidTagAttachLongFilename
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongFilename
api_type:
- HeaderDef
ms.assetid: 83b69e8f-0b5a-4992-b5b8-160d3bdfa22a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 45b6b3fb0c67d854fddf3773c06cef7b36f54992
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339329"
---
# <a name="pidtagattachlongfilename-canonical-property"></a>Propiedad canónica PidTagAttachLongFilename

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre de archivo largo y la extensión de un archivo adjunto, excluyendo la ruta de acceso. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W  <br/> |
|Identificador:  <br/> |0x3707  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades pertenecen a los ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE y ATTACH_BY_REF_ONLY de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)). Las plataformas que admiten nombres de archivo largos deben establecer las propiedades **PR_ATTACH_LONG_FILENAME** y **PR_ATTACH_FILENAME** (  [PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) al enviar y deben comprobar PR_ATTACH_LONG_FILENAME primero al recibirlo. 
  
La aplicación cliente debe establecer esta propiedad en un nombre de archivo largo sugerido que se usará si el equipo host que recibe un mensaje admite nombres de archivo largos. **PR_ATTACH_LONG_FILENAME** puede usarse como nombre de archivo para guardar los datos adjuntos y para proporcionar la extensión de nombre de archivo si no se proporciona la propiedad **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)). 
  
A diferencia del nombre de **archivo PR_ATTACH_FILENAME,** este nombre no está restringido a un nombre de archivo de ocho caracteres más una extensión de tres caracteres. En su lugar, puede tener hasta 256 caracteres, incluido el nombre de archivo, la extensión y el punto separador. 
  
MAPI sólo funciona con nombres de archivo en el juego de caracteres ANSI. Las aplicaciones cliente que usan nombres de archivo en un juego de caracteres OEM deben convertirlos en ANSI antes de llamar a MAPI. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Especifica las propiedades de los mensajes codificados con derechos administrados.
    
[[MS-OJOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para representar mensajes de correo de voz y fax.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mmapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

