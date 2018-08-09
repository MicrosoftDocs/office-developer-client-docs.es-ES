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
ms.openlocfilehash: 519ee2b91275e4253845afa35a9a80470071966d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820182"
---
# <a name="pidtagrulestate-canonical-property"></a>Propiedad canónica PidTagRuleState

  
  
**Hace referencia a**: Outlook 
  
Un valor que se interpreta como una combinación de máscara de bits de marcadores que especifican el estado de la regla.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RULE_STATE  <br/> |
|Identificador:  <br/> |0x6677  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Reglas del servidor  <br/> |
   
## <a name="remarks"></a>Comentarios

En la tabla siguiente define los valores posibles de esta propiedad.
  
ES-es (ST_ENABLED, 0 x 00000001 de máscara de bits)
  
> La regla está habilitada para la ejecución. Si no se establece este indicador, el servidor debe omitir esta regla al evaluar las reglas.
    
Recuperación de emergencia (error, máscara de bits 0 x 00000002)
  
> El servidor ha encontrado un error al procesar la regla.
    
DE (ST_ONLY_WHEN_OOF, máscara de bits 0 x 00000004)
  
> La regla sólo se ejecuta cuando el usuario establece el estado de fuera de oficina (OOF) en el buzón de correo. Esta marca no se debe establecer en una regla de carpeta pública.
    
ALTA (ST_KEEP_OOF_HIST, máscara de bits 0 x 00000008)
  
> Esta marca no se debe establecer en una regla de carpeta pública.
    
EL (ST_EXIT_LEVEL, máscara de bits 0 x 00000010)
  
> Evaluación de la regla finalizará después de ejecutar esta regla, excepto para la evaluación de las reglas de fuera de la oficina.
    
SCL (ST_SKIP_IF_SCL_IS_SAFE, 0 x 00000020 de máscara de bits)
  
> Es posible que se omitió la evaluación de esta regla.
    
PE (ST_RULE_PARSE_ERROR, máscara de bits 0x00000040)
  
> El servidor ha encontrado un error al analizar los datos de regla proporcionados por el cliente.
    
X
  
> No se utiliza este protocolo. No se debe modificar este bit por el cliente.
    
Tenga en cuenta sobre la interacción entre ST_ONLY_WHEN_OOF y ST_EXIT_LEVEL indicadores: 
  
Cuando se establece el estado "fuera de la oficina" en el buzón de correo, y una condición de regla se evalúa como TRUE, 
  
Y:
  
- La regla tiene establecido el indicador ST_EXIT_LEVEL y no tiene marca ST_ONLY_WHEN_OOF. A continuación, el servidor no debe evaluar las reglas posteriores que no tienen ST_ONLY_WHEN_OOF marcador establecido y debe evaluar las reglas posteriores que tienen la marca ST_ONLY_WHEN_OOF establecida.
    
OR:
  
- La regla tiene marcas de la ST_EXIT_LEVEL y el ST_ONLY_WHEN_OOF establecer. A continuación, el servidor no debe evaluar las reglas posteriores.
    
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

