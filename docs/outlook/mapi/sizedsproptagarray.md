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
ms.openlocfilehash: f873ad5234460f9f1781c7427b60d285f7486196
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282701"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura [SPropTagArray](sproptagarray.md) con nombre que incluye un número especificado de etiquetas de propiedad. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Estructura relacionada:  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>Parameters

__CTAG_
  
> Número de etiquetas de propiedad que se van a incluir en la nueva estructura.
    
__nombre_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

Use la macro **SizedSPropTagArray** para crear una matriz de etiquetas de propiedad con límites explícitos. 
  
Para usar la nueva estructura que resulta de la macro **SizedSPropTagArray** como un puntero a una estructura **SPropTagArray** , realice la siguiente conversión: 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>Vea también

- [SPropTagArray](sproptagarray.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

