---
title: Celda ShapeShdwScaleFactor (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033175
localization_priority: Normal
ms.assetid: 94ec06c5-8d2f-dd27-1eed-1abaf93daba8
description: Especifica el porcentaje en que se puede aumentar o reducir la sombra de una forma.
ms.openlocfilehash: 0b6392030e7efc8ea36c8d728b99c9b82482840b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823192"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a>Celda ShapeShdwScaleFactor (sección Formato de relleno)

Especifica el porcentaje en que se puede aumentar o reducir la sombra de una forma.
  
## <a name="remarks"></a>Observaciones

Cada sombra tiene una ubicación de eje sombreada, que es un punto de la sombra que corresponde al eje de la forma. Por ejemplo, si el eje de una forma se encuentra en el centro de la forma, la ubicación de eje sombreada sería el punto en el centro de la sombra. Cuando se aplica la escala a sombras simples, ampliación se centra en la ubicación de eje sombreada; Cuando se aplica la escala a sombras oblicuas, ampliación se aplica en la dirección oblicua. 
  
Para establecer este valor para todas las formas de una página, utilice la celda ShdwScaleFactor de la sección de propiedades de página.
  
Este valor corresponde al valor del parámetro **Ampliación** del cuadro de diálogo **Sombra** (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Sombra** y, a continuación, en **Opciones de sombra**).
  
Para obtener una referencia a la celda ShapeShdwScaleFactor por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ShapeShdwScaleFactor  <br/> |
   
Para obtener una referencia desde un programa a la celda ShapeShdwScaleFactor por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowFill** <br/> |
|Índice de celda:  <br/> |**visFillShdwScaleFactor** <br/> |
   

