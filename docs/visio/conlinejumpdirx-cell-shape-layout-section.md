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
ms.openlocfilehash: 22b9366b750a85a76498b83880aac2b9b974e1ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415043"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a>Celda ConLineJumpDirX (Sección de diseño de la forma)

Determina la dirección del salto de línea para los saltos de línea que se producen en un conector dinámico horizontal de una forma.
  
|**Valor**|**Dirección del salto de línea**|**Constante de automatización**|
|:-----|:-----|:-----|
| comprendi  <br/> | Valor predeterminado de página  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | Arriba  <br/> |**visLOJumpDirXUp** <br/> |
| segundo  <br/> | Abajo  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>Comentarios

Para establecer la dirección horizontal predeterminada de *todos los* saltos de conector en una página, utilice la celda PageLineJumpDirX en la sección de diseño de página. 
  
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
   

