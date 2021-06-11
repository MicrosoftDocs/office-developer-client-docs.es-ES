---
title: Propiedad canónica PidTagRuleActions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleActions
api_type:
- COM
ms.assetid: 3ec4259a-8fe9-46c3-82b8-42c6907b8515
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ab246414f7caaf76f462d9b80e762fe614c77c21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278903"
---
# <a name="pidtagruleactions-canonical-property"></a>Propiedad canónica PidTagRuleActions

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el conjunto de acciones asociadas a la regla. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RULE_ACTIONS  <br/> |
|Identificador:  <br/> |0x6680  <br/> |
|Tipo de datos:  <br/> |PT_ACTIONS  <br/> |
|Área:  <br/> |Reglas del lado servidor  <br/> |
   
## <a name="remarks"></a>Comentarios

Las acciones se expresan como una acción de regla y el búfer de valores de propiedad contiene la estructura del búfer de datos de acción de regla empaquetada según se especifica en [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ImportProcs.cpp  <br/> |PropCopyMore, HrCopyActions  <br/> |Estas funciones muestran cómo analizar una propiedad PT_ACTIONS con el fin de copiar en otra propiedad.  <br/> |
   
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

