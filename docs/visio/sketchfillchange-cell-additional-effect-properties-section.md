---
title: Celda SketchFillChange (sección Propiedades de efecto adicional)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Determina la cantidad de aleatorización del relleno de la forma de la geometría de la forma al usar un efecto de boceto, como un porcentaje de la longitud de una sección. Si el valor de la celda SketchFillChange se establece en 0%, la geometría de límite del relleno de una forma coincide con la geometría de la forma. Si el valor es 100%, la geometría de límite del relleno de la forma no sigue la geometría de la forma.
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408078"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a>Celda SketchFillChange (sección Propiedades de efecto adicional)

Determina la cantidad de aleatorización del relleno de la forma de la geometría de la forma al usar un efecto de boceto, como un porcentaje de la longitud de una sección. Si el valor de la celda **SketchFillChange** se establece en 0%, la geometría de límite del relleno de una forma coincide con la geometría de la forma. Si el valor es 100%, la geometría de límite del relleno de la forma no sigue la geometría de la forma. 
  
## <a name="remarks"></a>Comentarios

Para obtener mejores resultados, el intervalo ideal de valores para la celda **SketchFillChange** está entre el 15% y el 50 %. Un valor inferior al 15% apenas se nota; un valor superior al 50 % es cada vez más aleatorio. 
  
Para obtener una referencia a la celda **SketchFillChange** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la **propiedad CellsU,** use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | SketchFillChange  <br/> |
   
Para obtener una referencia desde un programa a la celda **SketchFillChange** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice de celda:  <br/> |**visSketchFillChange** <br/> |
   

