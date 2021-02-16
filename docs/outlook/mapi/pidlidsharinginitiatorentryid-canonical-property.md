---
title: Propiedad canónica PidLidSharingInitiatorEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorEntryId
api_type:
- COM
ms.assetid: 47f00706-83df-49cb-bda7-ef572d76a020
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bfe682fc3263278c6e1d02a29a8b6432f41ac79e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309530"
---
# <a name="pidlidsharinginitiatorentryid-canonical-property"></a>Propiedad canónica PidLidSharingInitiatorEntryId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Designa como propiedad de un mensaje para compartir.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidSharingInitiatorEid  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Sharing  <br/> |
|Long ID (LID):  <br/> |0x00008A09  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Compartir  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad debe establecerse en el valor de la propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) para la libreta de direcciones del usuario que ha iniciado sesión actualmente (vea [[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)). 
  
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

