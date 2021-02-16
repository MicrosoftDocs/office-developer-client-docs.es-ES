---
title: Propiedad canónica PidLidSharingRemoteType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteType
api_type:
- COM
ms.assetid: e9bc7c7c-86df-45d8-922b-76e3b076144a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3297ca951097c9f3601086809c6e294854c88656
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331216"
---
# <a name="pidlidsharingremotetype-canonical-property"></a>Propiedad canónica PidLidSharingRemoteType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el tipo de la carpeta compartida remota. Esta es una propiedad de un mensaje para compartir.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidSharingRemoteType  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Sharing  <br/> |
|Long ID (LID):  <br/> |0x00008A1D  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Compartir  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad debe establecerse en el mismo valor que la propiedad **dispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) y debe omitirse.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Comparte carpetas de buzones entre clientes.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

