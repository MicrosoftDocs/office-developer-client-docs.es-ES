---
title: Celda Angle (Sección de transformación de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251196
localization_priority: Normal
ms.assetid: d05a001c-9001-90d9-5028-f38b90acc53e
description: 'Representa el actual ángulo de giro de la forma en relación con su forma principal. La fórmula predeterminada para determinar el ángulo de giro de una forma 1-D es: =ATAN2(YFin-YInicio,XFin-XInicio).'
ms.openlocfilehash: 85f64c6111b492940d278a5558508a2dea6b1e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341471"
---
# <a name="angle-cell-shape-transform-section"></a>Celda Angle (Sección de transformación de forma)

Representa el actual ángulo de giro de la forma en relación con su forma principal. La fórmula predeterminada para determinar el ángulo de giro de una forma 1-D es: =ATAN2(YFin-YInicio,XFin-XInicio).
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Angle por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Ángulo  <br/> |
   
Para obtener una referencia a la celda Angle por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowXFormOut** <br/> |
| Índice de celda:  <br/> |**visXFormAngle** <br/> |
   

