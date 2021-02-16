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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435911"
---
# <a name="slpstrarray"></a>SLPSTRArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de valores de cadena que se usan para describir una propiedad de tipo PT_MV_STRING8.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a>Miembros

 **cValues**
  
> Recuento de valores en la matriz a la que apunta el **miembro lppszA.** 
    
 **lppszA**
  
> Puntero a una matriz de cadenas de caracteres de 8 bits terminadas en null.
    
## <a name="remarks"></a>Comentarios

Para obtener más información acerca PT_MV_STRING8, vea [Lista de tipos de propiedad](property-types.md).
  
## <a name="see-also"></a>Consulte también



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

