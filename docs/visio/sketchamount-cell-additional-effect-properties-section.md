---
title: Celda SketchAmount (sección de propiedades de efecto adicionales)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Determina la cantidad de distorsión para un efecto de boceto, como un número entero entre 0 y 25.
ms.openlocfilehash: d5ae954f2eab48722c48c9bc4b3f640403dbb3ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823256"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a>Celda SketchAmount (sección de propiedades de efecto adicionales)

Determina la cantidad de distorsión para un efecto de boceto, como un número entero entre 0 y 25. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |La forma no tiene ningún efecto de boceto que se ha aplicado.  <br/> |
|1-25  <br/> |La forma tiene distorsión de esbozo que se ha aplicado, donde un valor de 1 es la mayoría distorsión y 25 es el menor.  <br/> |
   
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda **SketchAmount** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | SketchAmount  <br/> |
   
Para obtener una referencia a la celda **SketchAmount** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice de celda:  <br/> |**visSketchAmount** <br/> |
   

