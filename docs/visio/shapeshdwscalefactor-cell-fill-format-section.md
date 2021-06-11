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
ms.openlocfilehash: 5862b61ca1f5df25ca97bf8742b9e20bf45091a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436268"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a>Celda ShapeShdwScaleFactor (Sección de formato de relleno)

Especifica el porcentaje en que se puede aumentar o reducir la sombra de una forma.
  
## <a name="remarks"></a>Comentarios

Cada sombra tiene una ubicación de eje sombreada, que es un punto en la sombra que corresponde al eje de la forma. Por ejemplo, si el eje de una forma se encuentra en el centro de ésta, la ubicación de eje sombreada sería el punto que se encuentra en el centro de la sombra. Al aplicar escala a sombras sencillas, la ampliación se centra en la ubicación de patillas sombreadas; al aplicar escala a sombras oblicuas, la ampliación se aplica en la dirección oblicua. 
  
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
   

