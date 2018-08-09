---
title: Propiedad canónica PidTagCreateTemplates
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreateTemplates
api_type:
- HeaderDef
ms.assetid: d2530009-5de3-4872-a0a5-be1389c4206e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 82da274670c9266a746defcf6bbd5dbcf621901b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819400"
---
# <a name="pidtagcreatetemplates-canonical-property"></a>Propiedad canónica PidTagCreateTemplates

  
  
**Hace referencia a**: Outlook 
  
Contiene un objeto incrustado de tabla que contiene los identificadores de entrada de plantilla de cuadro de diálogo. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CREATE_TEMPLATES  <br/> |
|Identificador:  <br/> |0x3604  <br/> |
|Tipo de datos:  <br/> |PT OBJECT  <br/> |
|Área:  <br/> |Libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener información sobre qué plantilla se pueden crear objetos dentro de un contenedor, llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en esta propiedad. El objeto resultante es la tabla de uso único que proporciona a los identificadores de entrada para todas las plantillas que se pueden crear dentro del contenedor. 
  
Para crear los objetos de plantilla, se ha de llamar al método **CreateEntry** del objeto de contenedor en los valores de columna de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la tabla de uso único.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[IABContainer::CreateEntry](iabcontainer-createentry.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

