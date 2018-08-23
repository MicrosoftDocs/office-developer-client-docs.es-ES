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
ms.openlocfilehash: f1aa54c3364185d322137ef41f6aface31c5c556
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587421"
---
# <a name="pidtagdiscretevalues-canonical-property"></a>Propiedad canónica PidTagDiscreteValues

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si un informe de no entrega aplica a sólo a discretos miembros de una lista de distribución en lugar de toda la lista. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DISCRETE_VALUES  <br/> |
|Identificador:  <br/> |0x0E0E  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |MAPI no transmisible  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se usa dentro de un informe de no entrega cuando no se pudo entregar el mensaje a uno o varios miembros de una lista de distribución. Su objetivo es limitar la retransmisión intenta sólo los miembros individuales y no la lista de distribución como un todo. 
  
La tabla de destinatarios de un informe de no entrega contiene entradas para todos los destinatarios a quienes el mensaje no se pudo entregar y también para las listas de distribución, si lo hay, al que pertenecen. El proveedor de transporte debe establecer esta propiedad en TRUE para cada entrada de la lista de distribución, y deben copiar el **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) y el **PR_SEARCH_KEY** ([ PidTagSearchKey](pidtagsearchkey-canonical-property.md)) en la lista de distribución para **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) y **PR_ORIGINAL_SEARCH_KEY** ([ PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) propiedades para cada miembro de esa lista de distribución. 
  
 **PR_DISCRETE_VALUES** no se debe establecer para cualquier entrada destinatario del informe de no entrega que no sea una lista de distribución. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

