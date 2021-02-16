---
title: Propiedad canónica PidTagSearchFolderDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderDefinition
api_type:
- COM
ms.assetid: a61056e7-365c-4972-abf7-26e2ab07105d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3b4e5fa7228cf243c79a8ec0c9e2b73b7da21c6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336361"
---
# <a name="pidtagsearchfolderdefinition-canonical-property"></a>Propiedad canónica PidTagSearchFolderDefinition

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene datos que especifican los criterios de búsqueda.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_WB_SF_DEFINITION  <br/> |
|Identificador:  <br/> |0x6845  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Búsqueda  <br/> |
   
## <a name="remarks"></a>Comentarios

El contenido específico de cada campo del objeto binario grande (BLOB) contenido en esta propiedad depende del identificador de plantilla especificado en la propiedad **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)). Para obtener información acerca de la estructura BLOB y las plantillas de búsqueda, [vea [MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx). 
  
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

