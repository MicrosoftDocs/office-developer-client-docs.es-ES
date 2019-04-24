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
ms.openlocfilehash: 820df61ec23e2dd1459582e5a7bb35ad9525e0b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315823"
---
# <a name="pidtagabproviderid-canonical-property"></a>Propiedad canónica PidTagAbProviderId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una estructura [MAPIUID](mapiuid.md) del proveedor de la libreta de direcciones. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_AB_PROVIDER_ID  <br/> |
|Identificador:  <br/> |0x3615  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

La estructura **MAPIUID** identifica el proveedor de la libreta de direcciones que proporciona este contenedor en particular en la jerarquía de contenedores. El valor es único para cada proveedor. 
  
Un proveedor de libreta de direcciones puede proporcionar más de un identificador. Por ejemplo, un proveedor que proporciona dos contenedores diferentes puede publicar en **PR_AB_PROVIDER_ID** identificadores únicos para cada contenedor. 
  
 **PR_AB_PROVIDER_ID** es análogo a la propiedad **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para los almacenes de mensajes. Las aplicaciones cliente pueden usar **PR_AB_PROVIDER_ID** para buscar filas relacionadas en una tabla de jerarquías de la libreta de direcciones. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[Propiedad canónica PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)


[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

