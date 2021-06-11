---
title: Propiedad canónica PidTagConversationTopic
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationTopic
api_type:
- HeaderDef
ms.assetid: db852b99-ce04-49bf-a714-7549571502e2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dfd437fac3a784212807c495f6e8f1adbe759cb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334688"
---
# <a name="pidtagconversationtopic-canonical-property"></a>Propiedad canónica PidTagConversationTopic

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el tema del primer mensaje de un hilo de conversación. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W  <br/> |
|Identificador:  <br/> |0x0070  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

Un subproceso de conversación representa una serie de mensajes y respuestas. Estas propiedades se establecen para el primer mensaje de un subproceso, normalmente en la propiedad **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)). Los mensajes subsiguientes del subproceso deben usar el mismo tema sin modificaciones. 
  
La **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) indica la relación de orden entre mensajes y respuestas posteriores. Su uso es opcional, incluso si estas propiedades están establecidas. 
  
Un proveedor de almacén de mensajes tiene la opción de asegurar que estas propiedades siempre se establecen en los mensajes entrantes o salientes. Si estas propiedades ya están establecidas, no se deben modificar. Si no es así, se pueden establecer **en PR_NORMALIZED_SUBJECT**. Cualquier acción debe realizarse antes de [llamar a IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas en objetos de mensaje de correo electrónico.
    
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

