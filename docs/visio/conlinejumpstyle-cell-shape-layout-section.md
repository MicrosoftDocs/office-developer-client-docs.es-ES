---
title: Celda ConLineJumpStyle (Sección de diseño de la forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251655
localization_priority: Normal
ms.assetid: baa05a50-97d0-3769-635e-0ea20317d59a
description: Determina el estilo de salto de línea para los saltos de línea en un conector dinámico.
ms.openlocfilehash: ae8af4e326a6c895b3617a4869f98eaf0db68db1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415995"
---
# <a name="conlinejumpstyle-cell-shape-layout-section"></a>Celda ConLineJumpStyle (Sección de diseño de la forma)

Determina el estilo de salto de línea para los saltos de línea en un conector dinámico.
  
|**Valor**|**Estilo de salto de línea**|**Constante de automatización**|
|:-----|:-----|:-----|
|comprendi  <br/> |Valor predeterminado de página  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |Arcos  <br/> |**visLOJumpStyleArc** <br/> |
|segundo  <br/> |Gap  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Cuadrado  <br/> |**visLOJumpStyleSquare** <br/> |
|4   <br/> |Triangle  <br/> |**visLOJumpStyleTriangle** <br/> |
|5   <br/> |3 lados  <br/> |**visLOJumpStyle2Point** <br/> |
|6   <br/> |4 lados  <br/> |**visLOJumpStyle3Point** <br/> |
|7   <br/> |5 lados  <br/> |**visLOJumpStyle4Point** <br/> |
|8   <br/> |6 lados  <br/> |**visLOJumpStyle5Point** <br/> |
|9   <br/> |7 lados  <br/> |**visLOJumpStyle6Point** <br/> |
   
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
|Índice de celda:  <br/> |**visSLOJumpStyle** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de esta celda seleccionando un conector dinámico, haciendo clic en **comportamiento** en el grupo **diseño de formas** en la ficha [programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, haciendo clic en la pestaña **conector** . 
  
Para obtener una referencia a la celda ConLineJumpStyle por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ConLineJumpStyle  <br/> |
   
Para obtener una referencia desde un programa a la celda ConLineJumpStyle por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  

