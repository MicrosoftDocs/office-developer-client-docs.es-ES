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
ms.openlocfilehash: ae9b79abea9a1b2b31867b9ed575e16e8f1c4474
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412474"
---
# <a name="pidtagattachmimesequence-canonical-property"></a>Propiedad canónica PidTagAttachMimeSequence

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el número de secuencia MIME de los datos adjuntos de un mensaje MIME.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_MIME_SEQUENCE  <br/> |
|Identificador:  <br/> |0x3710  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Propiedades de datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se usa para la compatibilidad con MHTML. Representa el número de secuencia de los datos adjuntos dentro de la parte principal del cuerpo de varias partes MIME del mensaje MIME.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

