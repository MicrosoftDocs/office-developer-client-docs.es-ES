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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 6d2bb6bdb934e0b02831b813b1246a3df4193e0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820703"
---
# <a name="slpstrarray"></a>SLPSTRArray

  
  
**Se aplica a**: Outlook 
  
Contiene una matriz de valores de cadena que se utilizan para describir una propiedad de tipo PT_MV_STRING8.
  
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
  
> Recuento de valores de la matriz indicada por el miembro **lppszA** . 
    
 **lppszA**
  
> Puntero a una matriz de cadenas de caracteres de 8 bits terminado en null.
    
## <a name="remarks"></a>Notas

Para obtener más información sobre PT_MV_STRING8, vea la [Lista de tipos de propiedad](property-types.md).
  
## <a name="see-also"></a>Ver también



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

