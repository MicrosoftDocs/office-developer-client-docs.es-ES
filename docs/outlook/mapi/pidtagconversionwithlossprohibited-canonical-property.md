---
title: Propiedad canónica PidTagConversionWithLossProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversionWithLossProhibited
api_type:
- HeaderDef
ms.assetid: a18b560a-e054-45b3-946d-6504465db5b7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e5d9261a9f33d77d52cfd6e448e69a2c1e8df415
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585237"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a>Propiedad canónica PidTagConversionWithLossProhibited

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE si un agente de transferencia de mensajes (MTA) se prohíbe realizar las conversiones de texto que se pierdan la información de mensaje. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONVERSION_WITH_LOSS_PROHIBITED  <br/> |
|Identificador:  <br/> |0x000D  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Configuración general  <br/> |
   
## <a name="remarks"></a>Comentarios

Un ejemplo del tipo de conversión que se está prohibido es la asignación "con pérdida" de Unicode (dos bytes por carácter) a un conjunto de caracteres de un byte. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

