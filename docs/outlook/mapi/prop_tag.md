---
title: PROP_TAG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TAG
api_type:
- COM
ms.assetid: d8c9d18c-4043-41f3-8501-8be8e3a2c9ac
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cbead0a9953ae5106e1fcc7d07d965d4dc7bacb9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570992"
---
# <a name="proptag"></a>PROP_TAG

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una etiqueta de propiedad creada mediante la combinación de un tipo de propiedad especificado y un identificador. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a>Parámetros

_ulPropType_
  
> Tipo de propiedad para la nueva etiqueta de propiedad.
    
_ulPropID_
  
> Identificador de la propiedad para la nueva etiqueta de propiedad.
    
## <a name="remarks"></a>Comentarios

El **propiedades\_etiqueta** macro crea una etiqueta de propiedad para una propiedad de tipo _ulPropType_ y el identificador que se especifica en _ulPropID_. Por ejemplo, se puede crear una etiqueta de propiedad para un identificador de entrada mediante la macro **PROP_TAG** como sigue: 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

Los 16 bits de orden inferior de la etiqueta de propiedad devuelto contienen el tipo de propiedad, PT_BINARY, y los 16 bits de orden superior contienen el identificador de propiedad, 0xFFFF.
  
Para obtener más información acerca de las etiquetas de propiedad, vea [Etiquetas de propiedad MAPI](mapi-property-tags.md).
  
## <a name="see-also"></a>Recursos adicionales

- [SPropValue](spropvalue.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

