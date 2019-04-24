---
title: Propiedad canónica PidTagDetailsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 74eae4a4ed742c3bb90496f5975ad7dac6ff798f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360840"
---
# <a name="pidtagdetailstable-canonical-property"></a>Propiedad canónica PidTagDetailsTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un objeto de tabla de visualización incrustado.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DETAILS_TABLE  <br/> |
|Identificador:  <br/> |0x3605  <br/> |
|Tipo de datos:  <br/> |PT OBJECT  <br/> |
|Área:  <br/> |Contenedor de MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Si se pasa esta propiedad al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) para el objeto, se devuelve una interfaz [IMAPITable](imapitableiunknown.md) que permite la creación de la tabla de presentación. MAPI usa esta tabla para mostrar las hojas de propiedades de un objeto de la libreta de direcciones en respuesta a una llamada de [IAddrBook::D etails](iaddrbook-details.md) . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[Propiedad canónica PidTagSearch](pidtagsearch-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

