---
title: Celda PageRightMargin (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60062
localization_priority: Normal
ms.assetid: f864c759-ed94-8ab7-d664-cc04b3ed743e
description: Especifica el margen derecho de la página impresa.
ms.openlocfilehash: d30669626fe07379521d61554010ae1bd7b0e83a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440013"
---
# <a name="pagerightmargin-cell-print-properties-section"></a>Celda PageRightMargin (Sección de propiedades de impresión)

Especifica el margen derecho de la página impresa.
  
## <a name="remarks"></a>Comentarios

Este valor representa unidades físicas y no se ve afectado por escalas ni unidades de dibujo. Por ejemplo, si esta celda tiene el valor 0,25 pda., este margen será de 0,25 pulgadas incluso si se utilizan pies como unidades en la página. Si las unidades no se indican explícitamente, este valor asume de forma predeterminada las unidades de la página. 
  
Para obtener una referencia a la celda PageRightMargin por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PageRightMargin  <br/> |
   
Para obtener una referencia desde un programa a la celda PageRightMargin por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPrintProperties** <br/> |
| Índice de celda:  <br/> |**visPrintPropertiesRightMargin** <br/> |
   

