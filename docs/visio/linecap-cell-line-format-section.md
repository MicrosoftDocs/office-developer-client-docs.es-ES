---
title: Celda LineCap (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251231
localization_priority: Normal
ms.assetid: 3519216b-b6cf-2e8c-e20f-adfa373c9028
description: Indica si los remates de una línea son redondos, cuadrados o extendidos.
ms.openlocfilehash: 44de4bff87fd3d121dfce9eec934ec39bc61065a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425206"
---
# <a name="linecap-cell-line-format-section"></a>Celda LineCap (Sección de formato de línea)

Indica si los remates de una línea son redondos, cuadrados o extendidos.
  
|**Valor**|**Estilo de extremo de línea**|
|:-----|:-----|
|0  <br/> |Redondeada  <br/> |
|1   <br/> |Cuadrado  <br/> |
|2   <br/> |Extendido  <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de esta celda en el cuadro de diálogo **Línea** (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Línea**, seleccione **Flechas** y, a continuación, haga clic en **Más flechas**).
  
Para obtener una referencia a la celda LineCap por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LineCap  <br/> |
   
Para obtener una referencia desde un programa a la celda LineCap por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowLine** <br/> |
|Índice de celda:  <br/> |**visLineEndCap** <br/> |
   

