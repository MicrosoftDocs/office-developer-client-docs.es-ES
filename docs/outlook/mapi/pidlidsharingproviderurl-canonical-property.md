---
title: Propiedad canónica PidLidSharingProviderUrl
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingProviderUrl
api_type:
- COM
ms.assetid: d217ab33-d697-4d27-a962-08d551d301f0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1b906ce83e26326755b483382eec8e494cbe7875
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577369"
---
# <a name="pidlidsharingproviderurl-canonical-property"></a>Propiedad canónica PidLidSharingProviderUrl

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica la dirección URL que está relacionada con el proveedor de uso compartido e identificada por la propiedad **dispidSharingProviderGuid** ([PidLidSharingProviderGuid](pidlidsharingproviderguid-canonical-property.md)). Esto es una propiedad de un mensaje para compartir.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidSharingProviderUrl  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Sharing  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008A03  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Uso compartido  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se usa normalmente para proporcionar más información sobre el proveedor de uso compartido, pero se debe omitir.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Comparte las carpetas de buzón de correo entre los clientes.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

