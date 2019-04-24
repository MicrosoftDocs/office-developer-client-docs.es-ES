---
title: Propiedad canónica PidTagSearchFolderEfpFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderEfpFlags
api_type:
- COM
ms.assetid: ef82a75f-a09f-4880-ba6a-e739b16422a3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d670aa91cc60c051f8464f9d83536b888b44ca9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336431"
---
# <a name="pidtagsearchfolderefpflags-canonical-property"></a>Propiedad canónica PidTagSearchFolderEfpFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene las marcas de carpeta extendidas que se aplican al contenedor de la carpeta de búsqueda de la carpeta de búsqueda.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_WB_SF_EFP_FLAGS  <br/> |
|Identificador:  <br/> |0x6848  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Buscar   <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad debe contener expresamente los indicadores en la propiedad **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) y la subpropiedad **ExtendedFlags** en el campo b para la carpeta. Para obtener información acerca de las marcas de carpeta, vea [[ms-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para manipular una configuración de lista de carpetas de búsqueda.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Especifica la ubicación y las propiedades de los datos de configuración del cliente y el servidor, como las listas de categorías compartidas y las horas laborables.
    
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

