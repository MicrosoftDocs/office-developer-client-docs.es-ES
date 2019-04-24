---
title: Celda NewWindow (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
localization_priority: Normal
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: Especifica si el hipervínculo se abre en una ventana nueva.
ms.openlocfilehash: 0f9d1e4b1294dea3f211c8d0d69ffc49b6180066
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342234"
---
# <a name="newwindow-cell-hyperlinks-section"></a>Celda NewWindow (Sección de hipervínculos)

Especifica si el hipervínculo se abre en una ventana nueva.
  
|**Value**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | Abra la página vinculada, el documento o el sitio web en una ventana nueva.  <br/> |
| FALSE  <br/> | Valor predeterminado. No abrir una ventana nueva para el hipervínculo.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda NewWindow por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Hipervínculo.  *Nombre* . NewWindow donde HYPERLINK.  *Name* es el nombre de la fila  <br/> |
   
Para obtener una referencia desde un programa a la celda NewWindow por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionHyperlink** <br/> |
| Índice de fila:  <br/> |**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2,...  <br/> |
| Índice de celda:  <br/> |**visHLinkNewWin** <br/> |
   

