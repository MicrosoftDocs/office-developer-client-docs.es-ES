---
title: Celda ResizeMode (Sección de transformación de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
localization_priority: Normal
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: Muestra la configuración actual del comportamiento de cambio de tamaño para la forma.
ms.openlocfilehash: 7e9080fcd4604e2dbdc1dae31992f05e5b512213
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326883"
---
# <a name="resizemode-cell-shape-transform-section"></a>Celda ResizeMode (Sección de transformación de forma)

Muestra la configuración actual del comportamiento de cambio de tamaño para la forma.
  
|**Value**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|comprendi  <br/> |Usar la configuración del grupo.  <br/> |**visXFormResizeDontCare** <br/> |
|1  <br/> |Ajustar la posición únicamente.  <br/> |**visXFormResizeSpread** <br/> |
|segundo  <br/> |Cambiar la escala con el grupo.  <br/> |**visXFormResizeScale** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer este valor en la ficha **comportamiento** del cuadro de diálogo **comportamiento** (en la ficha [programador](run-in-developer-mode-display-the-developer-tab.md), en el grupo **diseño de formas** , haga clic en **comportamiento**). Para obtener una referencia a la celda ResizeMode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ResizeMode  <br/> |
   
Para obtener una referencia desde un programa a la celda ResizeMode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowXFormOut** <br/> |
|Índice de celda:  <br/> |**visXFormResizeMode** <br/> |
   

