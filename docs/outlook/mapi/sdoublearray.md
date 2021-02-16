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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 91440d619c8ad8a64b2bac7463a26d9c196a3c0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439271"
---
# <a name="sdoublearray"></a>SDoubleArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de dobles que se usa para describir una propiedad de tipo PT_MV_DOUBLE.
  
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
  
> Recuento de valores de la matriz a la que apunta el **miembro lpdbl.** 
    
 **lpdbl**
  
> Puntero a una matriz de valores dobles.
    
## <a name="remarks"></a>Comentarios

Para obtener más información acerca PT_MV_DOUBLE, vea [Lista de tipos de propiedad](property-types.md).
  
## <a name="see-also"></a>Consulte también



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

