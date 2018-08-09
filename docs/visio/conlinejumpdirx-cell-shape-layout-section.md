---
title: Celda ConLineJumpDirX (Sección de diseño de la forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Determina la dirección del salto de línea para los saltos de línea que se producen en un conector dinámico horizontal de una forma.
ms.openlocfilehash: 396830d0da22c15f036f95808b3a94c33e9dc5bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821835"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a>Celda ConLineJumpDirX (sección Diseño de forma)

Determina la dirección del salto de línea para los saltos de línea que se producen en un conector dinámico horizontal de una forma.
  
|**Valor**|**Dirección del salto de línea**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Valor predeterminado de página  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | Arriba  <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | Abajo  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>Comentarios

Para establecer el valor predeterminado dirección horizontal para el conector de *todos los* saltos de una página, utilice la celda PageLineJumpDirX en la sección de diseño de página. 
  
Para obtener una referencia a la celda ConLineJumpDirX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ConLineJumpDirX  <br/> |
   
Para obtener una referencia desde un programa a la celda ConLineJumpDirX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
| Índice de celda:  <br/> |**visSLOJumpDirX** <br/> |
   

