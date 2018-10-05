---
title: Propiedad canónica PidTagRtfSyncPrefixCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncPrefixCount
api_type:
- COM
ms.assetid: c2b15ac5-9e89-4ee2-812d-102d0b2ac56e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 61683534504b7451f126591af149d11306cff1bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389816"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a>Propiedad canónica PidTagRtfSyncPrefixCount

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene un recuento de los caracteres puede pasar por alto que aparecen antes de los caracteres del mensaje significativos.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RTF_SYNC_PREFIX_COUNT  <br/> |
|Identificador:  <br/> |0x1010  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mensaje MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

El número de caracteres de prefijo no incluya espacios en blanco.
  
Esta propiedad es una propiedad auxiliar de formato de texto enriquecido (RTF). Propiedades auxiliares RTF se usan por la función [RTFSync](rtfsync.md) y no están diseñadas para usarse directamente por las aplicaciones cliente. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

