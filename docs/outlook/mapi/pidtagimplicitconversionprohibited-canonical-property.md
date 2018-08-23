---
title: Propiedad canónica PidTagImplicitConversionProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImplicitConversionProhibited
api_type:
- HeaderDef
ms.assetid: c6cb5a86-0105-4743-9f8e-b832e898da52
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7635dd24f4fbc5128d3d96556802ab2e3fe56e35
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571846"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a>Propiedad canónica PidTagImplicitConversionProhibited

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si un agente de transferencia de mensajes (MTA) no puede crear mensaje implícita las conversiones de texto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_IMPLICIT_CONVERSION_PROHIBITED  <br/> |
|Identificador:  <br/> |0x0016  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Servidor  <br/> |
   
## <a name="remarks"></a>Comentarios

Si esta propiedad es TRUE, el sistema de mensajería no debe realizar ninguna conversión del contenido en el mensaje a menos que lo solicita explícitamente en una base por destinatario con la propiedad **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)).
  
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

