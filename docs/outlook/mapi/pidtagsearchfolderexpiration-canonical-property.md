---
title: Propiedad canónica PidTagSearchFolderExpiration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderExpiration
api_type:
- COM
ms.assetid: e5746090-c850-4e95-b1e7-a07e42c87179
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a119bb735f752719d292371d4dc43e72450b33c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336473"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a>Propiedad canónica PidTagSearchFolderExpiration

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la hora en la que el contenedor de la carpeta de búsqueda estará obsoleto y se debe actualizar o volver a crear.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_WB_SF_EXPIRATION  <br/> |
|Identificador:  <br/> |0x683A  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Búsqueda  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad debe tener el formato de número de minutos desde la medianoche hora universal coordinada (UTC) del 1 de enero de 1601.
  
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

