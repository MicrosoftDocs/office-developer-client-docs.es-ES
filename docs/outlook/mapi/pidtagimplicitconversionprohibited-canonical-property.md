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
ms.openlocfilehash: a0e18ef529b65317abd9446408ed73638c792809
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420671"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a>Propiedad canónica PidTagImplicitConversionProhibited

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si se prohíbe que un agente de transferencia de mensajes (MTA) haga conversiones implícitas de texto de mensajes.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_IMPLICIT_CONVERSION_PROHIBITED  <br/> |
|Identificador:  <br/> |0x0016  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Servidor  <br/> |
   
## <a name="remarks"></a>Comentarios

Si esta propiedad es TRUE, el sistema de mensajería no debe realizar ninguna conversión de contenido en el mensaje a menos que se solicite explícitamente por destinatario con la propiedad **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

