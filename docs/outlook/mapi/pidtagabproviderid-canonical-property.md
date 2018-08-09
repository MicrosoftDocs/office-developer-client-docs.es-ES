---
title: Propiedad canónica PidTagAbProviderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagAbProviderId
api_type:
- HeaderDef
ms.assetid: 23cfd1d0-8e9d-4508-93dd-a88c0ef77c51
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 84a2d5517d405ac6deb61f7c4679d6816e802404
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819155"
---
# <a name="pidtagabproviderid-canonical-property"></a>Propiedad canónica PidTagAbProviderId

  
  
**Hace referencia a**: Outlook 
  
Contiene la estructura [MAPIUID](mapiuid.md) de un proveedor libreta de direcciones. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_AB_PROVIDER_ID  <br/> |
|Identificador:  <br/> |0x3615  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

La estructura **MAPIUID** identifica qué proveedor de libreta de direcciones proporciona este contenedor determinado en la jerarquía del contenedor. El valor es único para cada proveedor. 
  
Un proveedor de la libreta de direcciones puede proporcionar más de un identificador. Por ejemplo, un proveedor que suministran los dos contenedores diferentes puede publicar en **PR_AB_PROVIDER_ID** identificadores únicos para cada contenedor. 
  
 **PR_AB_PROVIDER_ID** es análoga a la propiedad **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para los almacenes de mensajes. Las aplicaciones de cliente pueden usar **PR_AB_PROVIDER_ID** para buscar filas relacionadas en una tabla de jerarquías de la libreta de direcciones. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[Propiedad canónica PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)


[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

