---
title: Propiedad canónica PidTagAttachMimeSequence
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMimeSequence
api_type:
- HeaderDef
ms.assetid: d2a84f24-b4a5-4e16-9219-7a579a31a8f8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b8fe0dd61247d3473db4cc728ecfa2c83682b691
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587722"
---
# <a name="pidtagattachmimesequence-canonical-property"></a>Propiedad canónica PidTagAttachMimeSequence

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el número de secuencia MIME de un adjunto de mensaje MIME.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_MIME_SEQUENCE  <br/> |
|Identificador:  <br/> |0x3710  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Propiedades de datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se utiliza para compatibilidad con MHTML. Representa el número de secuencia de los datos adjuntos en el elemento primario parte MIME con varias partes del cuerpo del mensaje MIME.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

