---
title: Celda BulletSize (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
localization_priority: Normal
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: Especifica el tamaño de una viñeta.
ms.openlocfilehash: e1b6bd1b4535a70bf99b9cd90af3e0d52128da01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821676"
---
# <a name="bulletsize-cell-paragraph-section"></a>Celda BulletSize (Sección de párrafo)

Especifica el tamaño de una viñeta. 
  
## <a name="remarks"></a>Comentarios

Este valor se puede especificar para viñetas predefinidas o personalizadas y como porcentaje o un valor concreto. 
  
Si el valor es cero (0), la viñeta tiene el mismo tamaño de fuente que la del primer carácter del párrafo. Si el valor es un porcentaje, la viñeta se mide como un porcentaje del tamaño de fuente del primer carácter del párrafo. Los números negativos se tratan como porcentajes.
  
Para obtener una referencia a la celda BulletSize por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Para.BulletFontSize [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia a la celda BulletSize por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionParagraph** <br/> |
| Índice de fila:  <br/> |**visRowParagraph** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visBulletFontSize** <br/> |
   

