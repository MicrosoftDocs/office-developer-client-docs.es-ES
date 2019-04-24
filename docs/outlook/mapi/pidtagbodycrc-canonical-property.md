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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350928"
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

El almacén de mensajes puede usar cualquier algoritmo CRC que genere un valor de PT_LONG. Debe calcular esta propiedad como parte del método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) cuando se ha establecido la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) por primera vez y siempre que se haya modificado posteriormente.
  
Una aplicación cliente usa **PR_BODY_CRC** para facilitar la comparación de las cadenas de texto de mensaje contenidas en las propiedades de **PR_BODY** o sus variantes. Mediante esta propiedad, el cliente puede detectar rápida y fácilmente cuándo cambia el texto del mensaje. Puede obtener ganancias de rendimiento considerables usando **PR_BODY_CRC** en lugar de obtener **PR_BODY** del almacén de mensajes y compararlo con una versión local. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

