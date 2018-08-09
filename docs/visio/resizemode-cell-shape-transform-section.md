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
ms.openlocfilehash: a32f5dbc935e85a49ab585073ca6a31215fd102a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823015"
---
# <a name="resizemode-cell-shape-transform-section"></a>Celda ResizeMode (sección Transformación de forma)

Muestra la configuración actual del comportamiento de cambio de tamaño para la forma.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Usar la configuración del grupo.  <br/> |**visXFormResizeDontCare** <br/> |
|1  <br/> |Ajustar la posición únicamente.  <br/> |**visXFormResizeSpread** <br/> |
|2  <br/> |Cambiar la escala con el grupo.  <br/> |**visXFormResizeScale** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer este valor en la ficha **comportamiento** en el cuadro de diálogo **comportamiento** (en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md), en el grupo **Diseño de formas** , haga clic en **comportamiento**). Para obtener una referencia a la celda ResizeMode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ResizeMode  <br/> |
   
Para obtener una referencia desde un programa a la celda ResizeMode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowXFormOut** <br/> |
|Índice de celda:  <br/> |**visXFormResizeMode** <br/> |
   

