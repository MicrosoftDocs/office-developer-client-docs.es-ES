---
title: Propiedad canónica PidTagExtendedRuleSizeLimit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleSizeLimit
api_type:
- HeaderDef
ms.assetid: 87186764-fb58-4cdf-804d-bb13c5a8cb65
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 347d84021b7e9ece925acb99e8b539ba608337a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316348"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a>Propiedad canónica PidTagExtendedRuleSizeLimit

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el tamaño máximo, en bytes, que el usuario puede acumular para una sola regla "extendida".
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_EXTENDED_RULE_SIZE_LIMIT  <br/> |
|Identificador:  <br/> |0x0E9B  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Rules  <br/> |
   
## <a name="remarks"></a>Comentarios

Si esta propiedad se establece en el objeto de inicio de sesión, el cliente debe mantener el tamaño de la propiedad **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) en el valor especificado por esta propiedad. Por el contrario, el servidor debe devolver un error si el cliente intenta establecer una propiedad binaria demasiado grande.
  
Para obtener información acerca de las reglas extendidas, vea [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Especifica las operaciones permitidas para los objetos principales del almacén de mensajes.
    
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

