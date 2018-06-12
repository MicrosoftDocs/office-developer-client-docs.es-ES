---
title: Propiedad canónico PidLidToDoTitle
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 66208b2d31ca379389f3249abf281dd4d040e276
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819010"
---
# <a name="pidlidtodotitle-canonical-property"></a>Propiedad canónico PidLidToDoTitle

  
  
**Se aplica a**: Outlook 
  
Contiene texto puede especificar el usuario para identificar este objeto de mensaje en una lista de tareas pendientes consolidada.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidToDoTitle  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x000085A4  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Tarea  <br/> |
   
## <a name="remarks"></a>Notas

Esta propiedad no se debe establecer en una tarea. Para indicar una propiedad vacía, no establezca esta propiedad en la cadena de longitud cero, pero en su lugar eliminarla. 
  
Al marcar un objeto de mensaje y la propiedad no existe, un cliente debe escribir el valor de **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) a esta propiedad.
  
En una lista de tareas pendientes consolidada, si esta propiedad no existe, un cliente debe sustituir el valor de la propiedad **PR_NORMALIZED_SUBJECT** al mostrar esta propiedad en la lista de tareas pendientes. 
  
En un objeto de mensaje de borrador, si el cliente implementa marcas de remitente, esta propiedad debe establecerse en el mismo valor que **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones relacionadas con marcas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Ver también



[Propiedad canónico PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
  
[Propiedad can�nico de PidLidFlagRequest](pidlidflagrequest-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

