---
title: Celda SketchAmount (sección Propiedades del efecto adicional)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Determina la cantidad de distorsión de un efecto de boceto, como un entero entre 0 y 25.
ms.openlocfilehash: fd9ee3390d05f24d81d9c6677160155b0f0f0d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404424"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a>Celda SketchAmount (sección Propiedades del efecto adicional)

Determina la cantidad de distorsión de un efecto de boceto, como un entero entre 0 y 25. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|comprendi  <br/> |La forma no tiene ningún efecto de boceto aplicado.  <br/> |
|1-25  <br/> |La forma tiene distorsión de boceto aplicada, donde un valor de 1 es la mayor distorsión y 25 es el mínimo.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **SketchAmount** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | SketchAmount  <br/> |
   
Para obtener una referencia desde un programa a la celda **SketchAmount** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice de celda:  <br/> |**visSketchAmount** <br/> |
   

