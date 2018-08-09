---
title: CURRENCY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CURRENCY
api_type:
- COM
ms.assetid: cffc05a0-95e4-4b9f-bf8f-c4272a75afa8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0789b566eb814fe984ae78670d22ad2937b0c3a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816630"
---
# <a name="currency"></a>CURRENCY

  
  
**Hace referencia a**: Outlook 
  
Contiene un entero de 64 bits con signo que representa un valor de moneda. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a>Members

 **Lo**
  
> 32 bits de orden inferior del valor de moneda. 
    
 **Hi**
  
> 32 bits de orden superior del valor de moneda.
    
## <a name="remarks"></a>Comentarios

La estructura de **moneda** es una representación de entero con escala de un número decimal con cuatro dígitos a la derecha del separador decimal. Por ejemplo, un valor almacenado de 327500 es interpretarse como que representa un valor de moneda de 32.7500. 
  
La estructura de **moneda** se usa para describir una propiedad de tipo PT_CURRENCY. Para obtener información acerca de los tipos de propiedad, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Vea también



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

