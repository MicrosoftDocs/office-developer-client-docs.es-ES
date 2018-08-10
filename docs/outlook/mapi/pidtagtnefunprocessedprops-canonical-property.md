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
ms.openlocfilehash: ee05f2e539d379e8fe197161fa0f6453add31afb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820392"
---
# <a name="pidtagtnefunprocessedprops-canonical-property"></a>Propiedad canónica PidTagTnefUnprocessedProps

  
  
**Hace referencia a**: Outlook 
  
Serializa las propiedades cuando el filtrado de formato de encapsulación neutro de transporte (TNEF).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_TNEF_UNPROCESSED_PROPS  <br/> |
|Identificador:  <br/> |0x0E9C  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |MAPI no transmisible  <br/> |
   
## <a name="remarks"></a>Comentarios

Se usa en Microsoft Outlook y Outlook Web Access (OWA) para guardar el TNEF original en los casos donde el TNEF contiene propiedades con nombre que no se puede crear en el almacén.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

