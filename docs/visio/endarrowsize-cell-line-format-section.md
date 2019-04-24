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
ms.openlocfilehash: 768a2b2adb05248049377eaee07194cdb89ed810
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328999"
---
# <a name="endarrowsize-cell-line-format-section"></a>Celda EndArrowSize (Sección de formato de línea)

Determina el tamaño de la punta de flecha que aparece en el extremo de la línea.
  
|**Value**|**Size**|**Constante de automatización**|
|:-----|:-----|:-----|
|comprendi  <br/> |Muy pequeño  <br/> |**visArrowSizeVerySmall** <br/> |
|1  <br/> |K.Esimo.Menor  <br/> |**visArrowSizeSmall** <br/> |
|segundo  <br/> |Mediano  <br/> |**visArrowSizeMedium** <br/> |
|3  <br/> |K.Esimo.Mayor  <br/> |**visArrowSizeLarge** <br/> |
|4  <br/> |Extragrande  <br/> |**visArrowSizeVeryLarge** <br/> |
|2,5  <br/> |Trama  <br/> |**visArrowSizeJumbo** <br/> |
|6,5  <br/> |Colossal  <br/> |**visArrowSizeColossal** <br/> |
   
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
   

