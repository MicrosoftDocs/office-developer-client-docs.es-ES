---
title: Propiedad canónica PidTagRuleState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleState
api_type:
- COM
ms.assetid: f62f3055-b855-4203-aa5c-6ba28b58c6f7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a0e15462cd3dc14c93155e34e47b7caac2c04087
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338615"
---
# <a name="pidtagrulestate-canonical-property"></a>Propiedad canónica PidTagRuleState

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Valor que se interpreta como una combinación de máscaras de bits de marcas que especifican el estado de la regla.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RULE_STATE  <br/> |
|Identificador:  <br/> |0x6677  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Reglas del lado servidor  <br/> |
   
## <a name="remarks"></a>Comentarios

En la tabla siguiente se definen los valores posibles de esta propiedad.
  
EN (ST_ENABLED, máscara de bits 0x00000001)
  
> La regla está habilitada para la ejecución. Si no se establece esta marca, el servidor debe omitir esta regla al evaluar reglas.
    
ER (ST_ERROR, máscara de bits 0x00000002)
  
> El servidor ha encontrado un error al procesar la regla.
    
OF (ST_ONLY_WHEN_OOF, máscara de bits 0x00000004)
  
> La regla solo se ejecuta cuando el usuario establece el estado De Office (OOF) en el buzón. Esta marca no debe establecerse en una regla de carpetas públicas.
    
HI (ST_KEEP_OOF_HIST, máscara de bits 0x00000008)
  
> Esta marca no debe establecerse en una regla de carpetas públicas.
    
EL (ST_EXIT_LEVEL, máscara de bits 0x00000010)
  
> La evaluación de reglas finalizará después de ejecutar esta regla, excepto para la evaluación de fuera de Office reglas.
    
SCL (ST_SKIP_IF_SCL_IS_SAFE, máscara de bits 0x00000020)
  
> Se puede omitir la evaluación de esta regla.
    
PE (ST_RULE_PARSE_ERROR, máscara de bits 0x00000040)
  
> El servidor ha encontrado un error al analizar los datos de regla proporcionados por el cliente.
    
X
  
> No se usa en este protocolo. El cliente no debe modificar este bit.
    
Nota sobre la interacción entre ST_ONLY_WHEN_OOF y ST_EXIT_LEVEL marcas: 
  
Cuando el estado "Fuera de Office" se establece en el buzón y una condición de regla se evalúa como TRUE, 
  
AND:
  
- La regla tiene el ST_EXIT_LEVEL de marca y no tiene ST_ONLY_WHEN_OOF de marca. A continuación, el servidor no debe evaluar las reglas posteriores que no tengan ST_ONLY_WHEN_OOF de marca y debe evaluar las reglas posteriores que ST_ONLY_WHEN_OOF marca establecida.
    
O:
  
- La regla tiene las marcas ST_EXIT_LEVEL y ST_ONLY_WHEN_OOF establecidas. A continuación, el servidor no debe evaluar ninguna regla posterior.
    
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

