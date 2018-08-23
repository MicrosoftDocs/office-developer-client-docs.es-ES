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
ms.openlocfilehash: 1b262ba9c83e9890719f716a373c566be172ae73
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572455"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
  
## <a name="see-also"></a>Recursos adicionales



[CURRENCY](currency.md)
  
[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

