---
title: Celda PagesY (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033790
localization_priority: Normal
ms.assetid: 396a0f3e-dbbb-3f5b-3c5d-f7dd454a765f
description: Determina el número de páginas impresas al que ajustar verticalmente la página de dibujo.
ms.openlocfilehash: 43d4081439525c516d3da28b6c0e46e9273d85c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429785"
---
# <a name="pagesy-cell-print-properties-section"></a>Celda PagesY (Sección de propiedades de impresión)

Determina el número de páginas impresas al que ajustar verticalmente la página de dibujo. 
  
## <a name="remarks"></a>Comentarios

Este valor se utiliza sólo cuando la celda OnPage tiene el valor TRUE. 
  
Para obtener una referencia a la celda PagesY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PagesY  <br/> |
   
Para obtener una referencia desde un programa a la celda PagesY por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPrintProperties** <br/> |
| Índice de celda:  <br/> |**visPrintPropertiesPagesY** <br/> |
   

