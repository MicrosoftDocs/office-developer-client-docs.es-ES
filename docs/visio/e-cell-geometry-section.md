---
title: Celda E (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251761
localization_priority: Normal
ms.assetid: bc0154b1-6930-1fe0-655c-05eab2d60230
description: Contiene la fórmula de una spline B racional no uniforme (NURBS).
ms.openlocfilehash: 5c9b3cbf96e2a218a8ed790d3a5615843360c95e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423569"
---
# <a name="e-cell-geometry-section"></a>Celda E (Sección de geometría)

Contiene la fórmula de una spline B racional no uniforme (NURBS).
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda E por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría  *i*  . E  *j*            donde  *i*  y  *j*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda E por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowVertex**  +   *j* donde *j* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visNURBSData** <br/> |
   

