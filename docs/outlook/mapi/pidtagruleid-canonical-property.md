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
ms.openlocfilehash: 8d88838893836c550136be9556299258b44e3e49
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359496"
---
# <a name="pidtagruleid-canonical-property"></a>Propiedad canónica PidTagRuleId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica un identificador único que el servidor de mensajería genera para cada regla cuando se crea la regla por primera vez. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RULE_ID  <br/> |
|Identificador:  <br/> |0x6674  <br/> |
|Tipo de datos:  <br/> |PT_I8  <br/> |
|Área:  <br/> |Reglas del lado servidor  <br/> |
   
## <a name="remarks"></a>Comentarios

El cliente no debe especificar esta propiedad al crear una regla nueva, pero debe especificarla al modificar o eliminar una regla.
  
Al eliminar una regla, la única propiedad que debe pasar el **cliente es PR_RULE_ID** y no debe pasar ninguna otra propiedad. El servidor debe omitir las propiedades que no son esta propiedad. Al agregar una regla, el cliente no debe pasar PR_RULE_ID **,** debe pasar las propiedades **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) y **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)). Al modificar una regla, el  cliente debe pasar PR_RULE_ID y pasar el resto de las propiedades que deben modificarse. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OJORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipula los mensajes de correo electrónico entrantes en un servidor.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedad canónica PidTagRuleCondition](pidtagrulecondition-canonical-property.md)
  
[Propiedad canónica PidTagRuleActions](pidtagruleactions-canonical-property.md)
  
[Propiedad canónica PidTagRuleProvider](pidtagruleprovider-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

