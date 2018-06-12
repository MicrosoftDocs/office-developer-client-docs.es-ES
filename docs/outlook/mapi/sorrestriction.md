---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 06b9b6a046aaa0f16418f75d402cc5be44f845a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820728"
---
# <a name="sorrestriction"></a>SOrRestriction

  
  
**Se aplica a**: Outlook 
  
Describe una restricción **o** que se usa para aplicar una operación **OR** lógica para una restricción. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a>Miembros

 **cRes**
  
> Recuento de las estructuras de la matriz indicada por el miembro **lpRes** . 
    
 **lpRes**
  
> Puntero a la estructura de [SRestriction](srestriction.md) que describe la restricción de combinarse mediante la operación de **OR** lógica. 
    
## <a name="remarks"></a>Notas

Para obtener más información acerca de la estructura **SOrRestriction** , vea [Acerca de las restricciones](about-restrictions.md). 
  
## <a name="see-also"></a>Ver también



[SRestriction](srestriction.md)


[Estructuras MAPI](mapi-structures.md)

