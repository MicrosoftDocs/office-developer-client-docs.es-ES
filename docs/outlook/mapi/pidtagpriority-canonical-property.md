---
title: Propiedad canónica PidTagPriority
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPriority
api_type:
- COM
ms.assetid: 0f3a628f-5f8e-4716-98cc-868bd3400ba9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b9c0f5ebeae21d6d683bbb5def727d29a34bcdb6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385455"
---
# <a name="pidtagpriority-canonical-property"></a>Propiedad canónica PidTagPriority

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene la prioridad relativa de un mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PRIORITY  <br/> |
|Identificador:  <br/> |0x0026  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Correo electrónico  <br/> |
   
## <a name="remarks"></a>Comentarios

No se deben confundir esta propiedad y la propiedad **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)). Importancia indica un valor a los usuarios, mientras que la prioridad indica el orden o la velocidad a la que se debe enviar el mensaje por el software del sistema de mensajería. Normalmente, una mayor prioridad indica un costo mayor. Mayor importancia generalmente se asocia con una presentación diferentes mediante la interfaz de usuario.
  
La prioridad de un mensaje de informe debe ser la misma que la prioridad del mensaje original se notifiquen.
  
Esta propiedad puede tener exactamente uno de los siguientes valores:
  
PRIO_NONURGENT 
  
> El mensaje no sea urgente.
    
PRIO_NORMAL 
  
> El mensaje tiene prioridad normal.
    
PRIO_URGENT 
  
> El mensaje es urgente.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.
    
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

