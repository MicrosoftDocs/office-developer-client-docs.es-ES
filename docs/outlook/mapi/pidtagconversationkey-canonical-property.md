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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389767"
---
# <a name="pidtagconversationkey-canonical-property"></a>Propiedad canónica PidTagConversationKey

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene la clave de conversación que se usa en Microsoft Outlook sólo al localizar **IPM. Objeto** mensajes, como el mensaje que contiene el historial de descarga para una cuenta de protocolo de oficina de correos (POP3). Esta propiedad ha quedado obsoleto en Microsoft Exchange Server. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONVERSATION_KEY  <br/> |
|Identificador:  <br/> |0x000B  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

Al obtener acceso a mensajes de correo electrónico como las conversaciones y la conversión de propiedades del mensaje al [Formato de encapsulación neutro para el transporte (TNEF)](transport-neutral-encapsulation-format-tnef.md), no utilice esta propiedad; en su lugar, use las propiedades [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) y [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canónicas. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones de protocolo de Microsoft Exchange Server relacionadas.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Subárbol IPM](ipm-subtree.md)
  
[Carpetas especiales de MAPI](mapi-special-folders.md)
  
[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

