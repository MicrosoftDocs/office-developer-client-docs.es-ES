---
title: Propiedad canónica PidTagNull
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNull
api_type:
- HeaderDef
ms.assetid: 192cdab8-c615-47b9-9f04-a1414eaf0c77
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7e9c3340dfad47a811b56c86e8e6104fb6aac7c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329270"
---
# <a name="pidtagnull-canonical-property"></a>Propiedad canónica PidTagNull

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Representa un valor nulo o un valor de una propiedad o reserva espacio de matriz.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_NULL  <br/> |
|Identificador:  <br/> |0x0000  <br/> |
|Tipo de datos:  <br/> |PT_NULL  <br/> |
|Área:  <br/> |Común  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se usa para reservar espacio en matrices de [estructuras SPropValue.](spropvalue.md) Se usa en una matriz de estructuras [SPropTagArray](sproptagarray.md) para decir al método que reserve espacio en la matriz devuelta de **estructuras SPropValue.** Esto permite que las propiedades calculadas se llenen de forma económica. 
  
Para obtener más información, vea [Información general sobre el tipo de propiedad MAPI.](mapi-property-type-overview.md)
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas en los contactos y listas de distribución personales.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

