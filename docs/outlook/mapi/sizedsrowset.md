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
ms.openlocfilehash: cb1e19a3f3703dc4943a5f6c322f1c8b429da5fa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410934"
---
# <a name="sizedsrowset"></a>SizedSRowSet

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura [SRowSet con](srowset.md) nombre que contiene un número especificado de filas. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionada:  <br/> |**SRowSet** <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a>Parámetros

_ _resalte_
  
> Recuento del número de filas que se incluirán en la nueva estructura.
    
_ _name_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

Para usar la nueva estructura que resulta de la macro **SizedSRowSet** como puntero a una estructura **SRowSet,** realice la conversión siguiente: 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a>Consulte también

- [SRowSet](srowset.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

