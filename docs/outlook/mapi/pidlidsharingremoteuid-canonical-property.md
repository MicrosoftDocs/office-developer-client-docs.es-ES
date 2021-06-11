---
title: Propiedad canónica PidLidSharingRemoteUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteUid
api_type:
- COM
ms.assetid: cfe3b728-317b-4871-adea-e2fdf8441da7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c3e783934367ad7c5c1a9a760aa8a24525901832
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331265"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a>Propiedad canónica PidLidSharingRemoteUid

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el identificador de entrada de la carpeta remota que se va a compartir. Esta es una propiedad de un mensaje de uso compartido.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidSharingRemoteUid  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Sharing  <br/> |
|Id. largo (LID):  <br/> |0x00008A06  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Compartir  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad debe establecerse en la representación de cadena hexadecimal del valor de la propiedad PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la carpeta que se comparte. Esta es una propiedad de un mensaje de uso compartido.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Comparte carpetas de buzones entre clientes.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

