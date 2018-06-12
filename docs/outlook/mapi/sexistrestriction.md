---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 62b5a42a540a4fb96761c45cd51c510f12225e9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820655"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**Se aplica a**: Outlook 
  
Describe una restricción existente que se usa para comprobar si una propiedad determinada existe como una columna en la tabla. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a>Miembros

 **ulReserved1**
  
> Reservado; debe ser cero. 
    
 **ulPropTag**
  
> Etiqueta de la propiedad que identifica la columna que se va a la existencia de cada fila.
    
 **ulReserved2**
  
> Reservado; debe ser cero.
    
## <a name="remarks"></a>Notas

La restricción de existen se usa para garantizar resultados significativos para otros tipos de restricciones que impliquen propiedades, por ejemplo, restricciones de propiedad y contenido. Cuando se pasa una restricción que implica una propiedad a [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md) y la propiedad no existe, no están definidos los resultados de la restricción. Mediante la creación de una restricción **y** que se une a la restricción de propiedad con una restricción existe, un autor de la llamada se pueda garantizar resultados precisos. 
  
Existen restricciones no se puede usar con las propiedades del objeto subcaracterística que tienen tipo pt Object. 
  
Para obtener más información acerca de la estructura **SExistRestriction** , vea [Acerca de las restricciones](about-restrictions.md). 
  
## <a name="see-also"></a>Ver también



[SRestriction](srestriction.md)


[Estructuras MAPI](mapi-structures.md)

