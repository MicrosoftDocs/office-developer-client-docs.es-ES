---
title: Propiedad canónica PidTagConversationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 00c65dae9bc29fe9cdb310b819ba99d6d46ebfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334702"
---
# <a name="pidtagconversationkey-canonical-property"></a>Propiedad canónica PidTagConversationKey

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la clave de conversación que se usa en Microsoft Outlook solo al buscar **IPM. Mensajes de MessageManager,** como el mensaje que contiene el historial de descargas de una cuenta de Protocolo de oficina de correos (POP3). Esta propiedad ha quedado en desuso en Microsoft Exchange Server. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONVERSATION_KEY  <br/> |
|Identificador:  <br/> |0x000B  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

Al obtener acceso a los mensajes de correo electrónico como conversaciones y convertir las propiedades del mensaje al formato de encapsulación neutro para transporte [(TNEF),](transport-neutral-encapsulation-format-tnef.md)no use esta propiedad; en su lugar, use [las propiedades canónicas PidTagConversationIndex](pidtagconversationindex-canonical-property.md) y [PidTagConversationTopic.](pidtagconversationtopic-canonical-property.md) 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Microsoft Exchange Server protocolo relacionados.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas en los objetos de mensaje de correo electrónico.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica y descodifica objetos de mensaje y datos adjuntos a una representación de secuencia eficiente.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Subárbol IPM](ipm-subtree.md)
  
[Carpetas especiales mapi](mapi-special-folders.md)
  
[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

