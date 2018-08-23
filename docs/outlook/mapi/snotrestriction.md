---
title: SNotRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SNotRestriction
api_type:
- COM
ms.assetid: e86ca032-d973-4b79-976e-5240ab38a0da
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 174da93e7682246565b12c4fc4ffa6d1a9de065c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575066"
---
# <a name="snotrestriction"></a>SNotRestriction

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción **no** , que se usa para aplicar una operación **NOT** lógica a una restricción. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a>Members

 **ulReserved**
  
> [entrada] Reservado; debe ser cero.
    
 **lpRes**
  
> Puntero a una estructura de [SRestriction](srestriction.md) que describa la restricción esté unido al operador **NOT** lógico. 
    
## <a name="remarks"></a>Comentarios

Para obtener más información acerca de la estructura **SNotRestriction** , vea [Acerca de las restricciones](about-restrictions.md). 
  
## <a name="see-also"></a>Recursos adicionales



[SRestriction](srestriction.md)


[Estructuras MAPI](mapi-structures.md)

