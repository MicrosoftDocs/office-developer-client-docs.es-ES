---
title: Propiedad canónica PidTagSearchFolderTemplateId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderTemplateId
api_type:
- COM
ms.assetid: 56288f55-b3ba-42df-9c90-f9b5857f19a1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bee22a7a435b99f4b94473a3f6eb4b7f32517128
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387205"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a>Propiedad canónica PidTagSearchFolderTemplateId

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador de la plantilla que se utiliza para la búsqueda.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_WB_SF_TEMPLATE_ID  <br/> |
|Identificador:  <br/> |0x6841  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Búsqueda  <br/> |
   
## <a name="remarks"></a>Comentarios

Criterios de carpeta de búsqueda se especifica mediante una plantilla. Esta propiedad en el mensaje que define la carpeta de búsqueda identifica la plantilla correspondiente. Además de definir los criterios de búsqueda, una plantilla también define las carpetas para excluir de la búsqueda, define los elementos que se deben excluir de la búsqueda y especifica el valor de **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).
  
Para obtener más información acerca de las plantillas de la carpeta de búsqueda, vea [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.
    
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

