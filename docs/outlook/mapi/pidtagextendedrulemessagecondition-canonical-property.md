---
title: Propiedad canónica PidTagExtendedRuleMessageCondition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageCondition
api_type:
- HeaderDef
ms.assetid: 891851e1-e4a4-4c20-a26c-7223bcca35f7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 81ac1cb85e64b4ecdcf63997d4bdcd0f45b3364b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819493"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a>Propiedad canónica PidTagExtendedRuleMessageCondition

  
  
**Hace referencia a**: Outlook 
  
Contiene información acerca de las propiedades con nombre que se encuentran dentro de las condiciones de regla extendida.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_EXTENDED_RULE_MSG_CONDITION  <br/> |
|Identificador:  <br/> |0x0E9A  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Rules  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad debe establecerse en un mensaje FAI. Sirve para el mismo propósito como **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), pero contiene información adicional acerca de las propiedades con nombre que se usa. Todos los valores de cadena contenidos en cualquier parte del valor de esta propiedad de condición deben estar en formato Unicode.
  
Para obtener información acerca del formato de esta propiedad binaria, vea [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
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



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

