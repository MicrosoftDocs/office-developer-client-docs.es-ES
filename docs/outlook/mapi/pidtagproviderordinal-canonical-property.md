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
ms.openlocfilehash: fbeb63bbae23f8f7f78c92d3abed6bea1c3ac85d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438354"
---
# <a name="pidtagproviderordinal-canonical-property"></a>Propiedad canónica PidTagProviderOrdinal

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el índice de base cero de la posición de un proveedor de servicios en la tabla del proveedor.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROVIDER_ORDINAL  <br/> |
|Identificador:  <br/> |0x300D  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mapi común  <br/> |
   
## <a name="remarks"></a>Comentarios

MAPI calcula esta propiedad.
  
Obtenga la tabla del proveedor llamando al [método IMsgServiceAdmin::GetProviderTable.](imsgserviceadmin-getprovidertable.md) Ordene la tabla del proveedor en esta propiedad para mostrar el orden de transporte. 
  
## <a name="related-resources"></a>Recursos relacionados

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

