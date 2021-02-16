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
ms.openlocfilehash: 67093cf456db9df5f9e939bdda9d2e44f248dadc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331237"
---
# <a name="pidtagrtfsynctrailingcount-canonical-property"></a>Propiedad canónica PidTagRtfSyncTrailingCount

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un recuento de los caracteres que se pueden pasar por alto que aparecen después de los caracteres significativos del mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RTF_SYNC_TRAILING_COUNT  <br/> |
|Identificador:  <br/> |0x1011  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mensaje MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es una propiedad auxiliar de formato de texto enriquecido (RFT). La función [RTFSync](rtfsync.md) usa estas propiedades y no están pensadas para que las usen directamente las aplicaciones cliente. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica y descodifica objetos de mensaje y datos adjuntos a una representación de secuencia eficiente.
    
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

