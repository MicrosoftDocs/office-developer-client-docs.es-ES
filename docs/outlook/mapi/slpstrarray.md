---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 987020bd6fd49fcba9453075cd502bd5cea4c3a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361155"
---
# <a name="slpstrarray"></a>SLPSTRArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de valores de cadena que se usan para describir una propiedad de tipo PT_MV_STRING8.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Número de valores de la matriz a los que señala el miembro **lppszA** . 
    
 **lppszA**
  
> Puntero a una matriz de cadenas de caracteres de 8 bits terminadas en NULL.
    
## <a name="remarks"></a>Comentarios

Para obtener más información acerca de PT_MV_STRING8, vea [lista de tipos de propiedades](property-types.md).
  
## <a name="see-also"></a>Vea también



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

