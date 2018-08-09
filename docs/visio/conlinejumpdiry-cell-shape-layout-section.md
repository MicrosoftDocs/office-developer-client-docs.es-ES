---
title: Celda ConLineJumpDirY (Sección de diseño de la forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
localization_priority: Normal
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: Determina la dirección del salto de línea para los saltos de línea que se producen en un conector dinámico vertical de una forma.
ms.openlocfilehash: 2d0c0964b52c9afbccc9cb507024825434702b6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821823"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a>Celda ConLineJumpDirY (sección Diseño de forma)

Determina la dirección del salto de línea para los saltos de línea que se producen en un conector dinámico vertical de una forma.
  
|**Valor**|**Dirección del salto de línea**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Valor predeterminado de página  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | Izquierda  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | Derecha  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Comentarios

Para establecer el valor predeterminado dirección vertical para conector *todos los* saltos de una página, utilice la celda PageLineJumpDirY en la sección de diseño de página. 
  
Para obtener una referencia a la celda ConLineJumpDirY por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ConLineJumpDirY  <br/> |
   
Para obtener una referencia desde un programa a la celda ConLineJumpDirY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
| Índice de celda:  <br/> |**visSLOJumpDirY** <br/> |
   

