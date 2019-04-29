---
title: Propiedad canónica PidTagServiceExtraUids
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceExtraUids
api_type:
- COM
ms.assetid: 4838a9af-7818-49aa-ace8-cb94dda8471f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0fb688e2a845186224c1802f9df2ac537d5bb4d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422309"
---
# <a name="pidtagserviceextrauids-canonical-property"></a>Propiedad canónica PidTagServiceExtraUids

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una lista de las estructuras de [MAPIUID](mapiuid.md) que identifican secciones de perfil adicionales para el servicio de mensajes. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SERVICE_EXTRA_UIDS  <br/> |
|Identificador:  <br/> |0x3D0D  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Se pueden crear nuevas secciones de perfil para cada filtro de mensajes. Cuando la información sobre el servicio de mensajes se va a copiar a otro perfil, es importante copiar también las secciones de perfil adicionales para los filtros. Un proveedor de servicios que usa secciones de perfil adicionales puede almacenar las estructuras **MAPIUID** de esas secciones de perfil en **PR_SERVICE_EXTRA_UIDS**, lo que permite a MAPI copiar la información adicional del servicio de mensajes.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

