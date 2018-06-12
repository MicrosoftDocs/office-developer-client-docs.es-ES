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
ms.openlocfilehash: b4d927e1970e994047df3cb89afa7799a825511d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822673"
---
# <a name="newwindow-cell-hyperlinks-section"></a>Celda NewWindow (Sección de hipervínculos)

Especifica si el hipervínculo se abre en una ventana nueva.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | Abre la página, el documento o el sitio Web vinculado en una ventana nueva.  <br/> |
| FALSE  <br/> | Valor predeterminado. No abrir una ventana nueva para el hipervínculo.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda NewWindow por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Hipervínculo.  *Nombre* . NewWindow donde hipervínculo.  *Nombre* es el nombre de fila  <br/> |
   
Para obtener una referencia a la celda NewWindow por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionHyperlink** <br/> |
| Índice de fila:  <br/> |**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2,...  <br/> |
| Índice de celda:  <br/> |**visHLinkNewWin** <br/> |
   

