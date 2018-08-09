---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8b7a93a9abb9a1c589ac7fdab3723c9c924eea0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820683"
---
# <a name="sizedsrowset"></a>SizedSRowSet

**Hace referencia a**: Outlook 
  
Crea una estructura de [SRowSet](srowset.md) con nombre que contiene un número especificado de filas. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |**SRowSet** <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a>Parámetros

__gallo_
  
> Recuento del número de filas que se deben incluir en la nueva estructura.
    
__nombre_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

Para usar la nueva estructura que el resultado de la macro **SizedSRowSet** como un puntero a una estructura **SRowSet** , realice la conversión de tipos siguiente: 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a>Vea también

- [SRowSet](srowset.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

