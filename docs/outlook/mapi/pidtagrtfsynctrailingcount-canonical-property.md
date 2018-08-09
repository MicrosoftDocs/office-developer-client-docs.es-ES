---
title: Propiedad canónica PidTagRtfSyncTrailingCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncTrailingCount
api_type:
- COM
ms.assetid: 3f0e5b24-767e-46f5-bb3d-e9cb82cb935b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3174ebbcf70104c82305e2a20df1e183d30265d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820143"
---
# <a name="pidtagrtfsynctrailingcount-canonical-property"></a>Propiedad canónica PidTagRtfSyncTrailingCount

  
  
**Hace referencia a**: Outlook 
  
Contiene un recuento de los caracteres puede pasar por alto que aparecen después de los caracteres del mensaje significativos.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RTF_SYNC_TRAILING_COUNT  <br/> |
|Identificador:  <br/> |0x1011  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mensaje MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es una propiedad auxiliar de formato de texto enriquecido (RTF). Estas propiedades se usan por la función [RTFSync](rtfsync.md) y no están diseñadas para usarse directamente por las aplicaciones cliente. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
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

