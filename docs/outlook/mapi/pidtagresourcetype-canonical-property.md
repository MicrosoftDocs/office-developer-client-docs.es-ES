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
ms.openlocfilehash: 56f14488812842d5e9fe63ae228c325059ebe679
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575094"
---
# <a name="pidtagresourcetype-canonical-property"></a>Propiedad canónica PidTagResourceType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor que indica el tipo de proveedor de servicio.
  
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
  
> Proveedor de la libreta de direcciones
    
MAPI_HOOK_PROVIDER 
  
> Proveedor de enlace de cola de impresión
    
MAPI_PROFILE_PROVIDER 
  
> Proveedor de perfiles
    
MAPI_SPOOLER 
  
> Cola de mensajes
    
MAPI_STORE_PROVIDER 
  
> Proveedor de almacén de mensajes
    
MAPI_SUBSYSTEM 
  
> Subsistema MAPI interno
    
MAPI_TRANSPORT_PROVIDER 
  
> Proveedor de transporte
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

