---
title: SCurrencyArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCurrencyArray
api_type:
- COM
ms.assetid: d28852ab-b542-40e1-b2ec-85d20a2eddfd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e9468d0c7fc7e46475afe19f12f225e53196639e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360700"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de valores de moneda que se usan para describir una propiedad de tipo PT_MV_CURRENCY. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Número de valores de la matriz a los que señala el miembro **lpcur** . 
    
 **lpcur**
  
> Puntero a una matriz de estructuras de [moneda](currency.md) que contienen los valores de moneda. 
    
## <a name="remarks"></a>Comentarios

Para obtener información sobre PT_MV_CURRENCY, vea [lista de tipos de propiedades](property-types.md). 
  
## <a name="see-also"></a>Vea también



[Visa](currency.md)
  
[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

