---
title: Celda LineJumpStyle (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251646
localization_priority: Normal
ms.assetid: 89f16674-ee1f-f5f9-9830-7bcc52e3a068
description: Determina el estilo de salto de línea de todos los conectores de la página de dibujo que no tengan un estilo de salto local.
ms.openlocfilehash: 96941f675b67b38a8575bd712db5ad0eb76cd50f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822465"
---
# <a name="linejumpstyle-cell-page-layout-section"></a>Celda LineJumpStyle (Sección de diseño de página)

Determina el estilo de salto de línea de todos los conectores de la página de dibujo que no tengan un estilo de salto local.
  
|**Valor**|**Estilo de salto de línea**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Arco  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |Arco  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Intervalo  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Cuadrado  <br/> |**visLOJumpStyleSquare** <br/> |
|4  <br/> |2 lados  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |3 lados  <br/> |**visLOJumpStyle2Point** <br/> |
|6  <br/> |4 lados  <br/> |**visLOJumpStyle3Point** <br/> |
|7  <br/> |5 lados  <br/> |**visLOJumpStyle4Point** <br/> |
|8  <br/> |6 lados  <br/> |**visLOJumpStyle5Point** <br/> |
|9  <br/> |7 lados  <br/> |**visLOJumpStyle6Point** <br/> |
   
## <a name="remarks"></a>Notas

También puede establecer el valor de esta celda en la ficha **Diseño y enrutamiento** en el cuadro de diálogo **Configurar página** (en la ficha **Diseño** , haga clic en la flecha de **Configurar página** y, a continuación, haga clic en **Diseño y enrutamiento**).
  
Para obtener una referencia a la celda LineJumpStyle por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LineJumpStyle  <br/> |
   
Para obtener una referencia a la celda LineJumpStyle por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPageLayout** <br/> |
|Índice de celda:  <br/> |**visPLOJumpStyle** <br/> |
   

