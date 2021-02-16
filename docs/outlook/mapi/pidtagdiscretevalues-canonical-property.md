---
title: Propiedad canónica PidTagDiscreteValues
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscreteValues
api_type:
- HeaderDef
ms.assetid: 958f3cf7-953a-43f4-9102-ad35edf5e813
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6d6974302e3413db3590abbbd3e6567976c6ac72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404844"
---
# <a name="pidtagdiscretevalues-canonical-property"></a>Propiedad canónica PidTagDiscreteValues

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si un informe de no entrega se aplica solo a miembros discretos de una lista de distribución en lugar de a toda la lista. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DISCRETE_VALUES  <br/> |
|Identificador:  <br/> |0x0E0E  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |MAPI no transmitible  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se usa dentro de un informe de no entrega cuando no se pudo entregar el mensaje a uno o más miembros de una lista de distribución. Su objetivo es limitar los intentos de retransmisión solo a esos miembros individuales y no a la lista de distribución en su totalidad. 
  
La tabla de destinatarios de un informe de no entrega contiene entradas para todos los destinatarios a los que no se pudo entregar el mensaje y también para las listas de distribución, si las hay, a las que pertenecen. El proveedor de transporte debe establecer esta propiedad en TRUE para cada entrada de lista de distribución y debe copiar las propiedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) y **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de la lista de distribución a **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) y **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) para cada miembro de esa lista de distribución. 
  
 **PR_DISCRETE_VALUES** no se debe establecer para ninguna entrada de destinatario de informe de no entrega que no sea una lista de distribución. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

