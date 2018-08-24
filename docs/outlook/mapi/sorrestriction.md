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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 054625601b496a8ec8f7745aa4cbc4715eed81a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585062"
---
# <a name="sorrestriction"></a>SOrRestriction

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Members

 **cRes**
  
> Recuento de las estructuras de la matriz indicada por el miembro **lpRes** . 
    
 **lpRes**
  
> Puntero a la estructura de [SRestriction](srestriction.md) que describe la restricción de combinarse mediante la operación de **OR** lógica. 
    
## <a name="remarks"></a>Comentarios

Para obtener más información acerca de la estructura **SOrRestriction** , vea [Acerca de las restricciones](about-restrictions.md). 
  
## <a name="see-also"></a>Vea también



[SRestriction](srestriction.md)


[Estructuras MAPI](mapi-structures.md)

