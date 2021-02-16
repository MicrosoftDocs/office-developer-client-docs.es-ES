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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336627"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a>Propiedad canónica PidTagSearchFolderTemplateId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador de la plantilla que se usa para la búsqueda.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_WB_SF_TEMPLATE_ID  <br/> |
|Identificador:  <br/> |0x6841  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Búsqueda  <br/> |
   
## <a name="remarks"></a>Comentarios

Los criterios de la carpeta de búsqueda se especifican mediante una plantilla. Esta propiedad del mensaje que define la carpeta de búsqueda identifica su plantilla correspondiente. Además de definir criterios de búsqueda, una plantilla también define las carpetas que se excluirán de la búsqueda, define los elementos que se excluirán de la búsqueda y especifica el valor de **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).
  
Para obtener más información acerca de las plantillas de carpeta de [búsqueda, vea [MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones para manipular una configuración de lista de carpetas de búsqueda.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

