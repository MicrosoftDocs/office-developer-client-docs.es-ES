---
title: Propiedad canónica PidTagCommonViewsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCommonViewsEntryId
api_type:
- HeaderDef
ms.assetid: cd9e6a46-2112-4663-891e-5e57b22c0950
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e22b8905901f16606614ac918896f3afe0093752
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437346"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a>Propiedad canónica PidTagCommonViewsEntryId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador de entrada de la carpeta de vista común predefinida. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_COMMON_VIEWS_ENTRYID  <br/> |
|Identificador:  <br/> |0x35E6  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Outlook aplicación  <br/> |
   
## <a name="remarks"></a>Comentarios

La carpeta de vista común contiene un conjunto predefinido de especificadores de vista estándar, mientras que la carpeta de vista contiene especificadores definidos por un usuario de mensajería. Estas carpetas, que no están visibles en la jerarquía de mensajes interpersonales (IPM), pueden contener muchos especificadores de vista, cada uno almacenado como mensaje. Una aplicación cliente puede elegir combinar los dos conjuntos de especificadores y hacer que ambos estén disponibles. 
  
Para obtener más información sobre las vistas, vea [Ver carpetas](mapi-view-folders.md).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)
  
[Propiedad canónica PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

