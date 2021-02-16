---
title: Propiedad canónica PidLidToDoTitle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7ed69d9bab84a5c572026bb9480249c1212e3376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339945"
---
# <a name="pidlidtodotitle-canonical-property"></a>Propiedad canónica PidLidToDoTitle

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene texto especificado por el usuario para identificar este objeto de mensaje en una lista de tareas que se ha consolidado.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidToDoTitle  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085A4  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad no debe establecerse en una tarea. Para indicar una propiedad vacía, no establezca esta propiedad en la cadena de longitud cero, sino que la elimine. 
  
Al marcar un objeto de mensaje y la propiedad no existe, un cliente debe escribir el valor de **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) en esta propiedad.
  
En una lista consolidada de tareas, si esta propiedad no existe, un cliente debe sustituir el valor de la propiedad **PR_NORMALIZED_SUBJECT** al mostrar esta propiedad en la lista de tareas. 
  
En un objeto de borrador de mensaje, si el cliente implementa marcas de remitente, esta propiedad debe establecerse en el mismo valor que **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a especificaciones Exchange Server protocolo relacionados
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones relacionadas con la marcación.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedad canónica PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
  
[Propiedad can�nico de PidLidFlagRequest](pidlidflagrequest-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

