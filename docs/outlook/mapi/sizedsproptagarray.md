---
title: SizedSPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropTagArray
api_type:
- COM
ms.assetid: 1d2dc6e9-735d-4b5b-af6f-adf6a32a666d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 363a85e1c6f111936b16e471eda6b9f962f8b65d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573624"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura de [elemento SPropTagArray](sproptagarray.md) con nombre que incluye un número especificado de etiquetas de propiedad. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>Parámetros

__ctag_
  
> Recuento de etiquetas de propiedad que se deben incluir en la nueva estructura.
    
__nombre_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

Use la macro **SizedSPropTagArray** para crear una matriz de etiqueta de propiedad con límites explícitos. 
  
Para usar la nueva estructura que el resultado de la macro **SizedSPropTagArray** como un puntero a una estructura de **elemento SPropTagArray** , realice la conversión de tipos siguiente: 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>Recursos adicionales

- [SPropTagArray](sproptagarray.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

