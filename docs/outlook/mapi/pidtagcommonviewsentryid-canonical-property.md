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
ms.openlocfilehash: 7449e59227b147d34c2329175d0251dbb9c427b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581345"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a>Propiedad canónica PidTagCommonViewsEntryId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador de entrada de la carpeta vista común predefinida. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_COMMON_VIEWS_ENTRYID  <br/> |
|Identificador:  <br/> |0x35E6  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Aplicación de Outlook  <br/> |
   
## <a name="remarks"></a>Comentarios

La carpeta de vista comunes contiene un conjunto predefinido de especificadores de vista estándar, mientras que la carpeta de la vista contiene especificadores definidos por un usuario de mensajería. Estas carpetas, que no están visibles en la jerarquía de mensajes interpersonales (IPM), pueden contener muchos especificadores de vista, cada uno de ellos que se almacene como un mensaje. Puede elegir una aplicación cliente combinar los dos conjuntos de especificadores y que estén ambos disponibles. 
  
Para obtener más información sobre vistas, consulte [Las carpetas de la vista](mapi-view-folders.md).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedad canónica PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)
  
[Propiedad canónica PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

