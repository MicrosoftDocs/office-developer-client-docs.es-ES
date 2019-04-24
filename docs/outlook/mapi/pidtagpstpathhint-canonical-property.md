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
ms.openlocfilehash: 6415ddcec2823192967b8869b46b22b58b08ba5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286360"
---
# <a name="pidtagpstpathhint-canonical-property"></a>Propiedad canónica PidTagPstPathHint

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona el nombre de la tabla de almacenamiento personal (archivo. pst), que el usuario puede editar, para el cuadro de diálogo Configuración. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W  <br/> |
|Identificador:  <br/> |0x6771  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Tabla de almacenamiento personal (. pst) interno  <br/> |
   
## <a name="remarks"></a>Comentarios

Si se usa la propiedad **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) en su lugar, se abrirá el cuadro de diálogo Configuración, pero el usuario no podrá editar la ruta de acceso y muchas otras propiedades.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]] 
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

