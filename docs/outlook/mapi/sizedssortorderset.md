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
ms.openlocfilehash: 60a335f85eea8778580e0bd74693a5c28591103c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282631"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura [SSortOrderSet](ssortorderset.md) con nombre que contiene un número especificado de criterios de ordenación. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Estructura relacionada:  <br/> |**SSortOrderSet** <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a>Parameters

__csort_
  
> Número de criterios de ordenación que se van a incluir en la nueva estructura.
    
__nombre_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

Use la macro **SizedSSortOrderSet** para crear un conjunto de orden con los límites explícitos. 
  
Para usar la nueva estructura que resulta de la macro **SizedSSortOrderSet** como un puntero a una estructura **SSortOrderSet** , realice la siguiente conversión: 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a>Vea también

- [SSortOrderSet](ssortorderset.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

