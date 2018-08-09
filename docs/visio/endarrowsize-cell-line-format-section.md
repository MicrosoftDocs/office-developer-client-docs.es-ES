---
title: Celda EndArrowSize (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251630
localization_priority: Normal
ms.assetid: e2ecf7c0-a0e9-951f-676a-8e5857bb6544
description: Determina el tamaño de la punta de flecha que aparece en el extremo de la línea.
ms.openlocfilehash: e03871c75857297634300c2eee091de2d0144903
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822085"
---
# <a name="endarrowsize-cell-line-format-section"></a>Celda EndArrowSize (sección Formato de línea)

Determina el tamaño de la punta de flecha que aparece en el extremo de la línea.
  
|**Valor**|**Size**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Muy pequeño  <br/> |**visArrowSizeVerySmall** <br/> |
|1  <br/> |Pequeño  <br/> |**visArrowSizeSmall** <br/> |
|2  <br/> |Medio  <br/> |**visArrowSizeMedium** <br/> |
|3  <br/> |Grande  <br/> |**visArrowSizeLarge** <br/> |
|4  <br/> |Extragrande  <br/> |**visArrowSizeVeryLarge** <br/> |
|5  <br/> |Enorme  <br/> |**visArrowSizeJumbo** <br/> |
|6  <br/> |Colosal  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer este valor en el cuadro de diálogo **Línea** (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Línea**, elija **Flechas** y, a continuación, haga clic en **Más flechas**).
  
Para obtener una referencia a la celda EndArrowSize por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |EndArrowSize  <br/> |
   
Para obtener una referencia a la celda EndArrowSize por su índice desde un programa, use la propiedad **CellsSRC** con los siguientes argumentos: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowLine** <br/> |
|Índice de celda:  <br/> |**visLineEndArrowSize** <br/> |
   

