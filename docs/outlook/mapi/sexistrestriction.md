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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 218238bea277a2d57c77fcc9d71cd622f7da42fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571951"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Members

 **ulReserved1**
  
> Reservado; debe ser cero. 
    
 **ulPropTag**
  
> Etiqueta de la propiedad que identifica la columna que se va a la existencia de cada fila.
    
 **ulReserved2**
  
> Reservado; debe ser cero.
    
## <a name="remarks"></a>Comentarios

La restricción de existen se usa para garantizar resultados significativos para otros tipos de restricciones que impliquen propiedades, por ejemplo, restricciones de propiedad y contenido. Cuando se pasa una restricción que implica una propiedad a [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md) y la propiedad no existe, no están definidos los resultados de la restricción. Mediante la creación de una restricción **y** que se une a la restricción de propiedad con una restricción existe, un autor de la llamada se pueda garantizar resultados precisos. 
  
Existen restricciones no se puede usar con las propiedades del objeto subcaracterística que tienen tipo pt Object. 
  
Para obtener más información acerca de la estructura **SExistRestriction** , vea [Acerca de las restricciones](about-restrictions.md). 
  
## <a name="see-also"></a>Recursos adicionales



[SRestriction](srestriction.md)


[Estructuras MAPI](mapi-structures.md)

