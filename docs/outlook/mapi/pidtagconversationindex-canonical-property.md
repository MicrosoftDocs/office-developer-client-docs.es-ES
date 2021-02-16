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
ms.openlocfilehash: c6fa0d8f1323e8562a78080f50dbf448b8019ec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334723"
---
# <a name="pidtagconversationindex-canonical-property"></a>Propiedad canónica PidTagConversationIndex

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor binario que indica la posición relativa de este mensaje dentro de un hilo de conversación. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONVERSATION_INDEX  <br/> |
|Identificador:  <br/> |0x0071  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

Un hilo de conversación representa una serie de mensajes y respuestas. Esta propiedad normalmente se implementa mediante valores de marca de tiempo concatenados. Su uso es opcional, incluso **si PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) está establecido. 
  
MAPI proporciona la [función ScCreateConversationIndex](sccreateconversationindex.md) para crear o actualizar un índice de conversación. La función toma el valor de índice actual como una matriz de bytes contada y devuelve el valor de índice con una marca de tiempo concatenada al final. Un mensaje que representa una respuesta a otro mensaje debe usar **ScCreateConversationIndex** para actualizar esta propiedad. 
  
Un proveedor de al almacenamiento de  mensajes tiene la opción de asegurar que PR_CONVERSATION_INDEX se establece siempre en los mensajes entrantes o salientes. Puede hacerlo llamando a **ScCreateConversationIndex**, ya sea con el valor existente si esta propiedad está establecida o con NULL si no lo está. Esta acción debe realizarse antes [de llamar a IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
  
Todos los mensajes que tienen el mismo valor para **PR_CONVERSATION_TOPIC** pueden ordenarse en esta propiedad para revelar la relación jerárquica de los mensajes. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas en los objetos de mensaje de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

