---
title: Celda SketchLineChange (sección de propiedades de efecto adicionales)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Determina la cantidad de selección aleatoria de línea de la forma en la geometría de la forma cuando se usa un efecto de boceto, como un porcentaje de la longitud de una sección. Si el valor de la celda SketchLineChange se establece en 0%, la geometría de la línea de la forma coincide con la geometría de la forma. Si el valor es 100%, la geometría de la línea de la forma no siguen la geometría de la forma.
ms.openlocfilehash: 57d2af1a914710d7e5a58686b577014ceb7af424
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823259"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a>Celda SketchLineChange (sección de propiedades de efecto adicionales)

Determina la cantidad de selección aleatoria de línea de la forma en la geometría de la forma cuando se usa un efecto de boceto, como un porcentaje de la longitud de una sección. Si el valor de la celda **SketchLineChange** se establece en 0%, la geometría de la línea de la forma coincide con la geometría de la forma. Si el valor es 100%, la geometría de la línea de la forma no siguen la geometría de la forma. 
  
## <a name="remarks"></a>Notas

Para obtener mejores resultados, el intervalo de valores de la celda **SketchLineChange** ideal está entre el 15% y un 50%. Un valor inferior al 15% es casi imperceptible; un valor mayor que el 50% pudo randomize demasiado la línea. 
  
Para obtener una referencia a la celda **SketchLineChange** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | SketchLineChange  <br/> |
   
Para obtener una referencia a la celda **SketchLineChange** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice de celda:  <br/> |**visSketchLineChange** <br/> |
   

