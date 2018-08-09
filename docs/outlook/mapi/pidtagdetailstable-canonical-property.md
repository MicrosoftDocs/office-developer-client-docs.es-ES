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
ms.openlocfilehash: a267f9a9fb8d97256cf7a448b453d04db2118180
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819432"
---
# <a name="pidtagdetailstable-canonical-property"></a>Propiedad canónica PidTagDetailsTable

  
  
**Hace referencia a**: Outlook 
  
Contiene un objeto de la tabla de presentación incrustada.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DETAILS_TABLE  <br/> |
|Identificador:  <br/> |0x3605  <br/> |
|Tipo de datos:  <br/> |PT OBJECT  <br/> |
|Área:  <br/> |Contenedor MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Pasa esta propiedad para el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para el objeto devuelve una interfaz [IMAPITable](imapitableiunknown.md) que permite la creación de la tabla para mostrar. MAPI utiliza esta tabla para mostrar las hojas de propiedades para un objeto de la libreta de direcciones en respuesta a una llamada de [IAddrBook::Details](iaddrbook-details.md) . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[Propiedad canónica PidTagSearch](pidtagsearch-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

