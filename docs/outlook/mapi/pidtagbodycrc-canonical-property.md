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
ms.openlocfilehash: 66a150cf3f83465840aa0e79a9ef921b1534f814
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819283"
---
# <a name="pidtagbodycrc-canonical-property"></a>Propiedad canónica PidTagBodyCrc

  
  
**Hace referencia a**: Outlook 
  
Contiene un valor de redundancia cíclica (CRC) de verificación en el texto del mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_BODY_CRC  <br/> |
|Identificador:  <br/> |0x0E1C  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentarios

El almacén de mensajes puede utilizar cualquier algoritmo CRC que genera un valor PT_LONG. Debe calcular esta propiedad como parte del método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) cuando se ha establecido la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) por primera vez y siempre que se ha modificado posteriormente.
  
Una aplicación cliente usa **PR_BODY_CRC** para facilitar la comparación de las cadenas de texto de mensaje contenidas en las propiedades **PR_BODY** o sus variantes. Uso de esta propiedad, el cliente puede rápida y fácilmente detectar cuándo ha cambiado el texto del mensaje. Pueden obtener mejoras significativas del rendimiento mediante el uso de **PR_BODY_CRC** en lugar de obtener **PR_BODY** desde el almacén de mensajes y la compara con una versión local. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

