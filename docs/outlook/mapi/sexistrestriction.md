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
ms.openlocfilehash: 6e3cdcf3579b26776d9e278bb339758d4f56d890
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418942"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción existente que se usa para probar si una propiedad determinada existe como una columna de la tabla. 
  
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
  
> Etiqueta de propiedad que identifica la columna que se va a probar para comprobar su existencia en cada fila.
    
 **ulReserved2**
  
> Reservado; debe ser cero.
    
## <a name="remarks"></a>Comentarios

La restricción existente se usa para garantizar resultados significativos para otros tipos de restricciones que implican propiedades, como restricciones de propiedad y contenido. Cuando una restricción que implica una propiedad se pasa a [IMAPITable::Restrict](imapitable-restrict.md) o [IMAPITable::FindRow](imapitable-findrow.md) y la propiedad no existe, los resultados de la restricción son indefinidos. Al crear una **restricción AND** que une la restricción de propiedad con una restricción existente, se pueden garantizar resultados precisos al autor de la llamada. 
  
Las restricciones existentes no se pueden usar con propiedades de subelementos que tengan propiedades de tipo PT_OBJECT. 
  
Para obtener más información acerca **de la estructura SExistRestriction,** vea [Acerca de las restricciones](about-restrictions.md). 
  
## <a name="see-also"></a>Consulte también



[SRestriction](srestriction.md)


[Estructuras MAPI](mapi-structures.md)

