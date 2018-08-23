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
ms.openlocfilehash: 9f8da0902ea4c4a862d279ee80ba566c0473c44e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592328"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción **y** , que se usa para unirse a un grupo de restricciones de uso de una operación de **AND** lógica. 
  
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

## <a name="members"></a>Members

 **cRes**
  
> Recuento de las restricciones de búsqueda en la matriz indicada por el miembro **lpRes** . 
    
 **lpRes**
  
> Puntero a una matriz de estructuras [SRestriction](srestriction.md) que se van a combinar con una operación de **AND** lógica. 
    
## <a name="remarks"></a>Comentarios

El resultado de la **SAndRestriction** es TRUE si todas las restricciones de sus secundarios se evalúan como TRUE. Es FALSE si algún tipo de restricción secundarios se evalúa como FALSE. 
  
Para obtener una descripción de los tipos de restricciones, cómo crearlas y código de ejemplo, vea [Acerca de las restricciones](about-restrictions.md).
  
## <a name="see-also"></a>Recursos adicionales



[SRestriction](srestriction.md)


[Estructuras MAPI](mapi-structures.md)

