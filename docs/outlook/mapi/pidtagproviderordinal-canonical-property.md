---
title: Propiedad canónica PidTagProviderOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderOrdinal
api_type:
- COM
ms.assetid: d062b54d-7c32-4369-ab69-f7193773a1c0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b56ee557884e12728c98827f9eb1a280d7a29c30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819974"
---
# <a name="pidtagproviderordinal-canonical-property"></a>Propiedad canónica PidTagProviderOrdinal

  
  
**Hace referencia a**: Outlook 
  
Contiene el índice de base cero de la posición de un proveedor de servicios en la tabla proveedor.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROVIDER_ORDINAL  <br/> |
|Identificador:  <br/> |0x300D  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI comunes  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se calcula mediante MAPI.
  
Obtener la tabla de proveedor llamando al método [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) . Ordenar la tabla de proveedor de esta propiedad para mostrar el orden de transporte. 
  
## <a name="related-resources"></a>Recursos relacionados

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

