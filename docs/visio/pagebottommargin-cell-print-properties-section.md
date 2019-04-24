---
title: Celda PageBottomMargin (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60060
localization_priority: Normal
ms.assetid: 7a97e97c-278d-2e1e-6c4f-f5f32e2cdeb0
description: Especifica el margen inferior de la página impresa.
ms.openlocfilehash: f546d89b8761c6c1b7340af69d2b48f16c180767
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334415"
---
# <a name="pagebottommargin-cell-print-properties-section"></a>Celda PageBottomMargin (Sección de propiedades de impresión)

Especifica el margen inferior de la página impresa.
  
## <a name="remarks"></a>Comentarios

Este valor representa unidades físicas y no se ve afectado por escalas ni unidades de dibujo. Por ejemplo, si esta celda tiene el valor 0,5 pulgadas, este margen será de 0,5 pulgadas incluso si se utilizan pies como unidades en la página. Si las unidades no se indican explícitamente, este valor asume de forma predeterminada las unidades de la página. 
  
Para obtener una referencia a la celda PageBottomMargin por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PageBottomMargin  <br/> |
   
Para obtener una referencia desde un programa a la celda PageBottomMargin por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPrintProperties** <br/> |
| Índice de celda:  <br/> |**visPrintPropertiesBottomMargin** <br/> |
   

