---
title: Celda SketchFillChange (sección Propiedades del efecto adicional)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Determina la cantidad de selección aleatoria de relleno de la forma de la geometría de forma cuando se usa un efecto de boceto, como un porcentaje de la longitud de una sección. Si el valor de la celda SketchFillChange se establece en 0%, la geometría del límite de relleno de la forma coincide con la geometría de la forma. Si el valor es 100%, la geometría del límite del relleno de la forma no siguen la geometría de la forma.
ms.openlocfilehash: 8dda34e03188909e167a4abda6f62da3d43c4dd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823264"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a>Celda SketchFillChange (sección Propiedades del efecto adicional)

Determina la cantidad de selección aleatoria de relleno de la forma de la geometría de forma cuando se usa un efecto de boceto, como un porcentaje de la longitud de una sección. Si el valor de la celda **SketchFillChange** se establece en 0%, la geometría del límite de relleno de la forma coincide con la geometría de la forma. Si el valor es 100%, la geometría del límite del relleno de la forma no siguen la geometría de la forma. 
  
## <a name="remarks"></a>Comentarios

Para obtener mejores resultados, el intervalo de valores de la celda **SketchFillChange** ideal está entre el 15% y un 50%. Un valor inferior al 15% es casi imperceptible; un valor mayor que 50% cada vez más es más aleatorio. 
  
Para obtener una referencia a la celda **SketchFillChange** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | SketchFillChange  <br/> |
   
Para obtener una referencia a la celda **SketchFillChange** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice de celda:  <br/> |**visSketchFillChange** <br/> |
   

