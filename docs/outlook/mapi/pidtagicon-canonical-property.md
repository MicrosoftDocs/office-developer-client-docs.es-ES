---
title: Propiedad canónica PidTagIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIcon
api_type:
- HeaderDef
ms.assetid: 815dabf3-3cac-40e1-b6ff-51db2ff5096a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ad8d6934b5e57429de5039e9420742caa9dd4294
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356731"
---
# <a name="pidtagicon-canonical-property"></a>Propiedad canónica PidTagIcon

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un mapa de bits de un icono de tamaño completo para un formulario. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ICON  <br/> |
|Identificador:  <br/> |0x0FFD  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |MAPI no transmitible  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad contiene una imagen de 32 × 32 píxeles de un icono, igual que el contenido de un archivo . Archivo ICO. Esta propiedad se copia normalmente desde el archivo . Archivo ICO especificado en la línea LargeIcon de la sección [Descripción] adecuada del archivo de configuración del formulario. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedad canónica PidTagMiniIcon](pidtagminiicon-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

