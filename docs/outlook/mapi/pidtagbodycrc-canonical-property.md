---
title: Propiedad canónica PidTagBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 416486c3b06c485a1fa6525b54c37a6e0d23f56c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415183"
---
# <a name="pidtagbodycrc-canonical-property"></a>Propiedad canónica PidTagBodyCrc

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor de comprobación de redundancia cíclica (CRC) en el texto del mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_BODY_CRC  <br/> |
|Identificador:  <br/> |0x0E1C  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentarios

El almacén de mensajes puede usar cualquier algoritmo CRC que genere un PT_LONG valor. Debe calcular esta propiedad como parte del método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) cuando la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) se haya establecido por primera vez y siempre que se haya modificado posteriormente.
  
Una aplicación cliente usa **PR_BODY_CRC** para ayudar a comparar cadenas de texto de mensaje contenidas **en PR_BODY** propiedades o sus variantes. Con esta propiedad, el cliente puede detectar de forma rápida y sencilla cuándo ha cambiado el texto del mensaje. Puede obtener ganancias significativas de rendimiento mediante  **PR_BODY_CRC** en lugar de obtener PR_BODY del almacén de mensajes y compararlo con una versión local. 
  
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

