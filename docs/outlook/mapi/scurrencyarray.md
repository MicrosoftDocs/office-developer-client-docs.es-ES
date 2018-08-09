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
ms.openlocfilehash: c440bb7d8f3d2d3002a4d1a80ca3a671b49f4d2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820605"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**Hace referencia a**: Outlook 
  
Contiene una matriz de valores de moneda que se utilizan para describir una propiedad de tipo PT_MV_CURRENCY. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Recuento de valores de la matriz indicada por el miembro **lpcur** . 
    
 **lpcur**
  
> Puntero a una matriz de estructuras de [moneda](currency.md) que contienen los valores de moneda. 
    
## <a name="remarks"></a>Comentarios

Para obtener información sobre PT_MV_CURRENCY, vea la [Lista de tipos de propiedad](property-types.md). 
  
## <a name="see-also"></a>Vea también



[CURRENCY](currency.md)
  
[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

