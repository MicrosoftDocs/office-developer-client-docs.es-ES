---
title: Celda SketchFillChange (sección Propiedades del efecto adicional)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Determina la cantidad de aleatoriedad del relleno de la forma a partir de la geometría de la forma al usar un efecto de boceto, como un porcentaje de la longitud de una sección. Si el valor de la celda SketchFillChange está establecido en 0%, la geometría de delimitación del relleno de una forma coincide con la geometría de la forma. Si el valor es 100%, la geometría de delimitación del relleno de la forma no sigue la geometría de la forma.
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339819"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a>Celda SketchFillChange (sección Propiedades del efecto adicional)

Determina la cantidad de aleatoriedad del relleno de la forma a partir de la geometría de la forma al usar un efecto de boceto, como un porcentaje de la longitud de una sección. Si el valor de la celda **SketchFillChange** está establecido en 0%, la geometría de delimitación del relleno de una forma coincide con la geometría de la forma. Si el valor es 100%, la geometría de delimitación del relleno de la forma no sigue la geometría de la forma. 
  
## <a name="remarks"></a>Comentarios

Para obtener los mejores resultados, el intervalo ideal de valores para la celda **SketchFillChange** está comprendido entre el 15% y el 50%. Un valor inferior al 15% es apenas perceptible; un valor superior a 50% es cada vez más aleatorio. 
  
Para obtener una referencia a la celda **SketchFillChange** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | SketchFillChange  <br/> |
   
Para obtener una referencia desde un programa a la celda **SketchFillChange** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice de celda:  <br/> |**visSketchFillChange** <br/> |
   

