---
title: SAndRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAndRestriction
api_type:
- COM
ms.assetid: 1b7dfe87-f87f-43e3-8332-a0d9c3f70d16
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da35c9c72f4cf3f076715a7a35a3e3514c672ceb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344663"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción **and** , que se usa para unir un grupo de restricciones mediante una operación lógica **and** . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a>Members

 **cRes**
  
> ReCuento de restricciones de búsqueda en la matriz a la que señala el miembro **lpRes** . 
    
 **lpRes**
  
> Puntero a una matriz de estructuras [SRestriction](srestriction.md) que se combinará con una operación lógica **and** . 
    
## <a name="remarks"></a>Comentarios

El resultado de **SAndRestriction** es true si todas sus restricciones secundarias se evalúan como true. Es FALSE si alguna restricción secundaria se evalúa como FALSE. 
  
Para obtener una descripción de los tipos de restricciones, cómo crearlos y el código de ejemplo, consulte [About Restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Vea también



[SRestriction](srestriction.md)


[Estructuras MAPI](mapi-structures.md)

