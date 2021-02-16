---
title: SCommentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCommentRestriction
api_type:
- COM
ms.assetid: 07631ae1-981e-4c8e-a30b-1213904fe079
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3f66f513cc16bc479dd24c53804d751a396141f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430612"
---
# <a name="scommentrestriction"></a>SCommentRestriction

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción de comentario, que se usa para anotar una restricción. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a>Miembros

 **cValues**
  
> Recuento de valores de propiedad en la matriz a la que apunta el **miembro lpProp.** 
    
 **lpRes**
  
> Puntero a una [estructura SRestriction.](srestriction.md) 
    
 **lpProp**
  
> Puntero a una matriz de [estructuras SPropValue,](spropvalue.md) cada una de las que contiene la etiqueta de propiedad y el valor de una propiedad con nombre. 
    
## <a name="remarks"></a>Comentarios

La **estructura SCommentRestriction** asocia un objeto con un conjunto de propiedades con nombre. Las restricciones de comentario son distintas de otras restricciones porque no se evalúan. Es decir, el método [IMAPITable::Restrict](imapitable-restrict.md) los omite. No hay ningún efecto en las filas devueltas por el método [IMAPITable::QueryRows](imapitable-queryrows.md) después de realizar una llamada **IMAPITable::Restrict.** 
  
La **estructura SCommentRestriction** se puede usar para mantener la información específica de la aplicación con una restricción cuando se guarda en el disco. Por ejemplo, un cliente que guarda el nombre de una propiedad con nombre usada en una restricción de propiedad puede hacerlo en una **estructura SCommentRestriction.** No es posible guardar un nombre de propiedad en una restricción de propiedad porque la estructura [SPropertyRestriction](spropertyrestriction.md) asociada contiene sólo la etiqueta de propiedad. 
  
Para obtener más información acerca **de la estructura SCommentRestriction** y las restricciones en general, vea [Acerca de las restricciones](about-restrictions.md). 
  
## <a name="see-also"></a>Consulte también



[SPropValue](spropvalue.md)
  
[SRestriction](srestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)


[Estructuras MAPI](mapi-structures.md)

