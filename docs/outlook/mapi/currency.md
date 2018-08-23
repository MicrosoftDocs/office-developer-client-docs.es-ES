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
ms.openlocfilehash: b5a2cd09942559167300d8a921987864b8c5e48f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576466"
---
# <a name="currency"></a>CURRENCY

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
  
## <a name="see-also"></a>Recursos adicionales



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

