---
title: Celda PageLeftMargin (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60061
localization_priority: Normal
ms.assetid: 7ecdfc37-c9d4-2fde-ed3e-be81657c24e2
description: Especifica el margen izquierdo de la página impresa.
ms.openlocfilehash: 5fd2c8cd5b18a4baedd355627005b7c5c2df3252
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822707"
---
# <a name="pageleftmargin-cell-print-properties-section"></a>Celda PageLeftMargin (Sección de propiedades de impresión)

Especifica el margen izquierdo de la página impresa.
  
## <a name="remarks"></a>Comentarios

Este valor representa unidades físicas y no se ve afectado por escalas ni unidades de dibujo. Por ejemplo, si esta celda tiene el valor 0,25 pda., este margen será de 0,25 pulgadas incluso si se utilizan pies como unidades en la página. Si las unidades no se indican explícitamente, este valor asume de forma predeterminada las unidades de la página. 
  
Para obtener una referencia a la celda PageLeftMargin por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PageLeftMargin  <br/> |
   
Para obtener una referencia a la celda PageLeftMargin por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPrintProperties** <br/> |
| Índice de celda:  <br/> |**visPrintPropertiesLeftMargin** <br/> |
   

