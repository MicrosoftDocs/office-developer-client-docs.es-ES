---
title: Propiedad canónica PidTagResourceType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceType
api_type:
- COM
ms.assetid: 48b634d7-deea-422b-8944-a8d929d83838
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1c7a35ded4861d724520b02ec5d61246774ca5cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434959"
---
# <a name="pidtagresourcetype-canonical-property"></a>Propiedad canónica PidTagResourceType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor que indica el tipo de proveedor de servicios.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RESOURCE_TYPE  <br/> |
|Identificador:  <br/> |0x3E03  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad puede tener exactamente uno de los siguientes valores:
  
MAPI_AB 
  
> Libreta de direcciones
    
MAPI_AB_PROVIDER 
  
> Proveedor de libreta de direcciones
    
MAPI_HOOK_PROVIDER 
  
> Proveedor de enlaces de cola
    
MAPI_PROFILE_PROVIDER 
  
> Proveedor de perfiles
    
MAPI_SPOOLER 
  
> Cola de mensajes
    
MAPI_STORE_PROVIDER 
  
> Proveedor de almacenamiento de mensajes
    
MAPI_SUBSYSTEM 
  
> Subsistema MAPI interno
    
MAPI_TRANSPORT_PROVIDER 
  
> Proveedor de transporte
    
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

