---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: cde59b73381458533910dc8f0a728cc4e6ca0c01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820607"
---
# <a name="sdoublearray"></a>SDoubleArray

  
  
**Se aplica a**: Outlook 
  
Contiene una matriz de tipo Double que se usa para describir una propiedad de tipo PT_MV_DOUBLE.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a>Miembros

 **cValues**
  
> Recuento de valores de la matriz indicada por el miembro **lpdbl** . 
    
 **lpdbl**
  
> Puntero a una matriz de valores de tipo double.
    
## <a name="remarks"></a>Notas

Para obtener más información sobre PT_MV_DOUBLE, vea la [Lista de tipos de propiedad](property-types.md).
  
## <a name="see-also"></a>Ver también



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

