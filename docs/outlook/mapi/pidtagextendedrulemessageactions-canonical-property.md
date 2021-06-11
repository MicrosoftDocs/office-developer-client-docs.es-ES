---
title: Propiedad canónica PidTagExtendedRuleMessageActions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageActions
api_type:
- HeaderDef
ms.assetid: 1cf277d4-76ec-4902-9e54-f1780cee49bf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 70f09d6db5940fcb9b980cc839988113bd3a3e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316341"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a>Propiedad canónica PidTagExtendedRuleMessageActions

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene información adicional acerca de las propiedades con nombre usadas en un mensaje De información asociada a carpetas (FAI).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_EXTENDED_RULE_MSG_ACTIONS  <br/> |
|Identificador:  <br/> |0x0E99  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Rules  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad debe establecerse en un mensaje fai. Esta propiedad tiene el mismo propósito que **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), pero contiene información adicional sobre la versión de la regla y las propiedades con nombre almacenadas en la acción de regla, así como información sobre las acciones que debe realizar esta regla. Todos los valores de cadena contenidos en cualquier parte del búfer de acciones usado para contener acciones deben estar en formato Unicode.
  
Para obtener información sobre el formato de esta propiedad binaria, vea [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipula los mensajes de correo electrónico entrantes en un servidor.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

