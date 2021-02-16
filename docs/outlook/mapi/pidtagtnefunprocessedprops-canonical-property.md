---
title: Propiedad canónica PidTagTnefUnprocessedProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefUnprocessedProps
api_type:
- COM
ms.assetid: df9cd614-1198-44a2-9bf5-36c57179a9a9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9ea9938ca9f8dd0b25cf2de5199178a76e17b6d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431326"
---
# <a name="pidtagtnefunprocessedprops-canonical-property"></a>Propiedad canónica PidTagTnefUnprocessedProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Serializa las propiedades al filtrar el formato de encapsulamiento neutro para transporte (TNEF).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_TNEF_UNPROCESSED_PROPS  <br/> |
|Identificador:  <br/> |0x0E9C  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |MAPI no transmitible  <br/> |
   
## <a name="remarks"></a>Comentarios

Lo usan Microsoft Outlook y Outlook Web Access (OWA) para guardar el TNEF original en los casos en los que el TNEF contiene propiedades con nombre que no se pueden crear en el almacén.
  
## <a name="related-resources"></a>Recursos relacionados

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

