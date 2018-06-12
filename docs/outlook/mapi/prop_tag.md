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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 9e53c39b713aa782eb387b85667f5ded6193006f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820436"
---
# <a name="proptag"></a>PROP_TAG

**Se aplica a**: Outlook 
  
Devuelve una etiqueta de propiedad creada mediante la combinación de un tipo de propiedad especificado y un identificador. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a>Sintaxis

_ulPropType_
  
> Tipo de propiedad para la nueva etiqueta de propiedad.
    
_ulPropID_
  
> Identificador de la propiedad para la nueva etiqueta de propiedad.
    
## <a name="remarks"></a>Notas

El **propiedades\_etiqueta** macro crea una etiqueta de propiedad para una propiedad de tipo _ulPropType_ y el identificador que se especifica en _ulPropID_. Por ejemplo, se puede crear una etiqueta de propiedad para un identificador de entrada mediante la macro **PROP_TAG** como sigue: 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

Los 16 bits de orden inferior de la etiqueta de propiedad devuelto contienen el tipo de propiedad, PT_BINARY, y los 16 bits de orden superior contienen el identificador de propiedad, 0xFFFF.
  
Para obtener más información acerca de las etiquetas de propiedad, vea [Etiquetas de propiedad MAPI](mapi-property-tags.md).
  
## <a name="see-also"></a>Ver también

- [SPropValue](spropvalue.md)
- [Macros relacionadas con las estructuras](macros-related-to-structures.md)

