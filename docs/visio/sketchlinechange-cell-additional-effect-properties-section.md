---
title: Celda SketchLineChange (sección Propiedades del efecto adicional)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Determina la cantidad de aleatorización de la línea de la forma a partir de la geometría de la forma al usar un efecto de boceto, como un porcentaje de la longitud de una sección. Si el valor de la celda SketchLineChange está establecido en 0%, la geometría de la línea de la forma coincide con la geometría de la forma. Si el valor es 100%, la geometría de la línea de la forma no sigue la geometría de la forma.
ms.openlocfilehash: ba57a4d2e43a91475f4c3ab4862f723eb2653a89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315130"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a>Celda SketchLineChange (sección Propiedades del efecto adicional)

Determina la cantidad de aleatorización de la línea de la forma a partir de la geometría de la forma al usar un efecto de boceto, como un porcentaje de la longitud de una sección. Si el valor de la celda **SketchLineChange** está establecido en 0%, la geometría de la línea de la forma coincide con la geometría de la forma. Si el valor es 100%, la geometría de la línea de la forma no sigue la geometría de la forma. 
  
## <a name="remarks"></a>Comentarios

Para obtener los mejores resultados, el intervalo ideal de valores para la celda **SketchLineChange** está comprendido entre el 15% y el 50%. Un valor inferior al 15% es apenas perceptible; un valor mayor que 50% podría aleatorizar demasiado la línea. 
  
Para obtener una referencia a la celda **SketchLineChange** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | SketchLineChange  <br/> |
   
Para obtener una referencia desde un programa a la celda **SketchLineChange** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice de celda:  <br/> |**visSketchLineChange** <br/> |
   

