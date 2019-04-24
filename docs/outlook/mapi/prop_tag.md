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
ms.openlocfilehash: 7ab4e4e9e51849037a91a071f16294cfdf10870c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328570"
---
# <a name="proptag"></a>PROP_TAG

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una etiqueta de propiedad creada mediante la combinación de un identificador y un tipo de propiedad especificados. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Estructura relacionada:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a>Parameters

_ulPropType_
  
> Tipo de propiedad para la nueva etiqueta de propiedad.
    
_ulPropID_
  
> Identificador de propiedad de la nueva etiqueta de propiedad.
    
## <a name="remarks"></a>Comentarios

La macro de la **etiqueta prop\_** crea una etiqueta de propiedad para una propiedad de tipo _ulPropType_ y el identificador especificado en _ulPropID_. Por ejemplo, se puede crear una etiqueta de propiedad para un identificador de entrada mediante la macro **PROP_TAG** de la siguiente manera: 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

Los 16 bits de orden inferior de la etiqueta de propiedad devuelta contienen el tipo de propiedad, PT_BINARY, y los 16 bits de orden superior contienen el identificador de la propiedad, 0xFFFF.
  
Para obtener más información acerca de las etiquetas de propiedad, consulte [MAPI Property Tags](mapi-property-tags.md).
  
## <a name="see-also"></a>Vea también

- [SPropValue](spropvalue.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

