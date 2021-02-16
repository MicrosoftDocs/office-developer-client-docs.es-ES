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
ms.openlocfilehash: dccb6b19af72d0f748a3a513b7f3d78904ebc789
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431123"
---
# <a name="currency"></a>CURRENCY

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un entero de 64 bits firmado que representa un valor de moneda. 
  
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

## <a name="members"></a>Miembros

 **Lo**
  
> Orden bajo 32 bits del valor de moneda. 
    
 **Hola**
  
> Orden alto 32 bits del valor de moneda.
    
## <a name="remarks"></a>Comentarios

La **estructura CURRENCY** es una representación de enteros con escala de un número decimal con cuatro dígitos a la derecha del separador decimal. Por ejemplo, un valor almacenado de 327500 se interpretará como un valor de moneda de 32,7500. 
  
La **estructura CURRENCY** se usa para describir una propiedad de tipo PT_CURRENCY. Para obtener información acerca de los tipos de propiedad, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Consulte también



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

