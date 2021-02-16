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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429351"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura [SPropTagArray con](sproptagarray.md) nombre que incluye un número especificado de etiquetas de propiedad. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionada:  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>Parámetros

_ _ctag_
  
> Número de etiquetas de propiedad que se incluirán en la nueva estructura.
    
_ _name_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

Use la macro **SizedSPropTagArray** para crear una matriz de etiquetas de propiedades con límites explícitos. 
  
Para usar la nueva estructura que resulta de la macro **SizedSPropTagArray** como puntero a una estructura **SPropTagArray,** realice la conversión siguiente: 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>Consulte también

- [SPropTagArray](sproptagarray.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

