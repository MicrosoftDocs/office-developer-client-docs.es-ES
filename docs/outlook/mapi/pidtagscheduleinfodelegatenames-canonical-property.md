---
title: Propiedad canónica PidTagScheduleInfoDelegateNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateNames
api_type:
- COM
ms.assetid: 592d9c78-4487-4c68-8ae7-4cd3d6265685
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a257934411bb11a30378ee46317d323156f53e31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314941"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a>Propiedad canónica PidTagScheduleInfoDelegateNames

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene los nombres de los delegados.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W  <br/> |
|Identificador:  <br/> |0x6844  <br/> |
|Tipo de datos:  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Área:  <br/> |Disponibilidad  <br/> |
   
## <a name="remarks"></a>Comentarios

Cada entrada de estas propiedades debe contener el valor de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la libreta de direcciones de cada delegado.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica métodos para conectarse y configurar buzones como delegados e interacciones con objetos de mensaje y calendario cuando actúan en nombre de otro usuario.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

