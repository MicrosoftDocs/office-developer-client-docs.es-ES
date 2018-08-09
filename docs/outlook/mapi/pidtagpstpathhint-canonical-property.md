---
title: Propiedad canónica PidTagPstPathHint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 9cb4af50-3735-4029-a608-a6e7927019dd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 295b20ebc0c41104a8b1c8e46e2064c3ef32f99e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819994"
---
# <a name="pidtagpstpathhint-canonical-property"></a>Propiedad canónica PidTagPstPathHint

  
  
**Hace referencia a**: Outlook 
  
Proporciona el nombre de tabla (archivos .pst) de almacenamiento personal, que el usuario puede editar, para el cuadro de diálogo de configuración. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W  <br/> |
|Identificador:  <br/> |0x6771  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Tabla de almacenamiento personal (.pst) interno  <br/> |
   
## <a name="remarks"></a>Comentarios

Si la propiedad **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) se usa en su lugar, se abrirá el cuadro de diálogo de configuración, pero el usuario no podrá editar la ruta de acceso y muchas otras propiedades.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]] 
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

