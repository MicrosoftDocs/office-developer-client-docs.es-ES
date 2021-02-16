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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438886"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción **AND,** que se usa para unirse a un grupo de restricciones mediante una operación **lógica AND.** 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a>Miembros

 **cRes**
  
> Recuento de restricciones de búsqueda en la matriz a la que apunta el **miembro lpRes.** 
    
 **lpRes**
  
> Puntero a una matriz [de estructuras SRestriction](srestriction.md) que se combinarán con una operación **lógica AND.** 
    
## <a name="remarks"></a>Comentarios

El resultado de **SAndRestriction** es TRUE si todas sus restricciones secundarias se evalúan en TRUE. Es FALSE si cualquier restricción secundaria se evalúa como FALSE. 
  
Para obtener una descripción de los tipos de restricciones, cómo crearlas y código de ejemplo, vea [Acerca de las restricciones](about-restrictions.md).
  
## <a name="see-also"></a>Consulte también



[SRestriction](srestriction.md)


[Estructuras MAPI](mapi-structures.md)

