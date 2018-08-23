---
title: Propiedad canónica PidTagConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationIndex
api_type:
- HeaderDef
ms.assetid: c65cdda7-9515-4da9-be75-43ebf45a02df
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 77fee834108a603c1cd10e8e47776cc34fd75a2b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584175"
---
# <a name="pidtagconversationindex-canonical-property"></a>Propiedad canónica PidTagConversationIndex

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor binario que indica la posición relativa de este mensaje dentro de una secuencia de conversación. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONVERSATION_INDEX  <br/> |
|Identificador:  <br/> |0x0071  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

Un subproceso de conversación representa una serie de mensajes y respuestas. Esta propiedad normalmente se implementa mediante los valores de marca de tiempo concatenado. Su uso es opcional, incluso si se establece **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)). 
  
MAPI proporciona la función [ScCreateConversationIndex](sccreateconversationindex.md) para crear o actualizar un índice de conversación. La función toma el valor de índice actual como una matriz de bytes contada y devuelve el valor de índice con una marca de tiempo concatenada al final. Un mensaje que representa una respuesta a otro mensaje debe usar **ScCreateConversationIndex** para actualizar esta propiedad. 
  
Un proveedor de almacén de mensajes tiene la opción de garantizar que **PR_CONVERSATION_INDEX** siempre se establece en los mensajes entrantes o salientes. Puede hacerlo mediante una llamada a **ScCreateConversationIndex**, con el valor existente si se establece esta propiedad o con el valor NULL si no lo está. Antes de llamar a [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , se debe realizar esta acción. 
  
Todos los mensajes que tienen el mismo valor para **PR_CONVERSATION_TOPIC** se pueden ordenar en esta propiedad para mostrar la relación jerárquica de los mensajes. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

