---
title: PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TYPE
api_type:
- COM
ms.assetid: 746d63fa-bfb7-479f-94dc-ba40011c1ec9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7bcaf230eed9cf21388b68f06ab678dc143f64ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571825"
---
# <a name="proptype"></a>PROP_TYPE

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve el tipo de propiedad de una etiqueta de propiedad especificado.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a>Parámetros

 _ulPropTag_
  
> Etiqueta de la propiedad que contiene el tipo de propiedad que se va a devolver.
    
## <a name="remarks"></a>Comentarios

La macro **PROP_TYPE** se puede usar para determinar el tipo de una propiedad. Por ejemplo, al llamar a los resultados de la PROP_TYPE (**entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))) en el valor PT_BINARY que se devuelven.
  
Cada etiqueta de la propiedad contiene el tipo de propiedad de la palabra de orden inferior (bits del 0 al 15) y el identificador de propiedad de la palabra de orden superior (bits 16 a 31). La macro **PROP_TYPE** extrae el tipo de propiedad y la coloca en los bits 0 a 15 del número entero que se va a devolver. Se establecen los bits restantes del valor devuelto a ceros. 
  
## <a name="see-also"></a>Recursos adicionales



[SPropValue](spropvalue.md)


[Macros relacionadas con estructuras](macros-related-to-structures.md)

