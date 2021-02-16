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
ms.openlocfilehash: 08cf1faa0c3cc4cf61e2253b0026361704fdd0e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438186"
---
# <a name="pidtagcreatetemplates-canonical-property"></a>Propiedad canónica PidTagCreateTemplates

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un objeto de tabla incrustado que contiene identificadores de entrada de plantilla de cuadro de diálogo. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CREATE_TEMPLATES  <br/> |
|Identificador:  <br/> |0x3604  <br/> |
|Tipo de datos:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener información sobre qué objetos de plantilla se pueden crear dentro de un contenedor, llame al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en esta propiedad. El objeto resultante es la tabla de uso único que proporciona los identificadores de entrada de todas las plantillas que puede crear dentro del contenedor. 
  
Para crear los objetos de plantilla, llame al método **CreateEntry** del objeto contenedor en los valores de columna **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la tabla de un solo elemento.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[IABContainer::CreateEntry](iabcontainer-createentry.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

