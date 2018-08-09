---
title: Propiedad canónica PidTagRuleId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleId
api_type:
- COM
ms.assetid: 341e8db0-52b7-4ba7-aaa6-eedf2783b4e8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 52a6132dcd6aa2c3a2951f3d1a6458808364dccb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820157"
---
# <a name="pidtagruleid-canonical-property"></a>Propiedad canónica PidTagRuleId

  
  
**Hace referencia a**: Outlook 
  
Especifica un identificador único que genera el servidor de mensajería para cada regla cuando se crea la regla por primera vez. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RULE_ID  <br/> |
|Identificador:  <br/> |0x6674  <br/> |
|Tipo de datos:  <br/> |PT_I8  <br/> |
|Área:  <br/> |Reglas del servidor  <br/> |
   
## <a name="remarks"></a>Comentarios

El cliente no debe especificar esta propiedad al crear una nueva regla, pero debe especificarlo al modificar o eliminar una regla.
  
Cuando se elimina una regla, la única propiedad que el cliente debe pasar es **PR_RULE_ID** y no debe pasar en cualquier otra propiedad. El servidor debe omitir las propiedades que no sean de esta propiedad. Al agregar una regla, el cliente no debe pasar en **PR_RULE_ID**, debe pasar el **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) y **PR_RULE_PROVIDER** ([ PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) propiedades. Al modificar una regla, el cliente debe pasar en **PR_RULE_ID** y debe pasar en el resto de las propiedades que deben modificarse. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipula los mensajes de correo electrónico entrante en un servidor.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagRuleCondition](pidtagrulecondition-canonical-property.md)
  
[Propiedad canónica PidTagRuleActions](pidtagruleactions-canonical-property.md)
  
[Propiedad canónica PidTagRuleProvider](pidtagruleprovider-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

