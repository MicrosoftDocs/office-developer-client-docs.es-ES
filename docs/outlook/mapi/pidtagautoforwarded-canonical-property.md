---
title: Propiedad canónica PidTagAutoForwarded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAutoForwarded
api_type:
- HeaderDef
ms.assetid: 1ba40cc2-ba27-4d75-9682-c536cf3a0d58
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 25d1bb121df6470f5038a2106587e3f5b37f6bb7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386365"
---
# <a name="pidtagautoforwarded-canonical-property"></a>Propiedad canónica PidTagAutoForwarded

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si el cliente solicita un campo de encabezado X-MS-Exchange-organización-AutoForwarded.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_AUTO_FORWARDED  <br/> |
|Identificador:  <br/> |0x0005  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Informe de errores general  <br/> |
   
## <a name="remarks"></a>Comentarios

Si esta propiedad está establecida en FALSE o no se utilizan, no se creará ningún campo de encabezado X-MS-Exchange-organización-AutoForwarded.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Define cada propiedad que se usa en los objetos que se describen en los documentos como prefijo MS-Oxobenc.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
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

