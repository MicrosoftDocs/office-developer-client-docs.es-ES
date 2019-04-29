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
ms.openlocfilehash: f86c77da62042d1bc2c0274564efa9fdb0887971
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404774"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a>Celda ConLineJumpDirY (Sección de diseño de la forma)

Determina la dirección del salto de línea para los saltos de línea que se producen en un conector dinámico vertical de una forma.
  
|**Valor**|**Dirección del salto de línea**|**Constante de automatización**|
|:-----|:-----|:-----|
| comprendi  <br/> | Valor predeterminado de página  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | Hacia la izquierda  <br/> |**visLOJumpDirYLeft** <br/> |
| segundo  <br/> | Derecha  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Comentarios

Para establecer la dirección vertical predeterminada para *todos los* saltos de conector en una página, utilice la celda PageLineJumpDirY en la sección de diseño de página. 
  
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
   

