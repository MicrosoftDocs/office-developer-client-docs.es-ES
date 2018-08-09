---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2eb92c3f1555407a77332bd6ec3b2b7202f0553f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820699"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**Hace referencia a**: Outlook 
  
Crea una estructura de [SSortOrderSet](ssortorderset.md) con nombre que contiene un número especificado de criterios de ordenación. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |**SSortOrderSet** <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a>Parámetros

__csort_
  
> Recuento de criterios de ordenación que se deben incluir en la nueva estructura.
    
__nombre_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

Use la macro **SizedSSortOrderSet** para crear un criterio de ordenación establecer con límites explícitos. 
  
Para usar la nueva estructura que el resultado de la macro **SizedSSortOrderSet** como un puntero a una estructura **SSortOrderSet** , realice la conversión de tipos siguiente: 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a>Vea también

- [SSortOrderSet](ssortorderset.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

