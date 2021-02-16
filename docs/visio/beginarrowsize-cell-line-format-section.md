---
title: Celda BeginArrowSize (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251629
localization_priority: Normal
ms.assetid: bfddb829-6e13-7d74-b9b9-2cb5c0937bae
description: Determina el tamaño de la punta de flecha que aparece en la parte inicial de la línea.
ms.openlocfilehash: 9c1288ced747c4e16090013cc043b040f1fbb59c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412285"
---
# <a name="beginarrowsize-cell-line-format-section"></a>Celda BeginArrowSize (Sección de formato de línea)

Determina el tamaño de la punta de flecha que aparece en la parte inicial de la línea.
  
|**Valor**|**Tamaño**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Muy pequeño  <br/> |**visArrowSizeVerySmall** <br/> |
| 1   <br/> | Pequeño  <br/> |**visArrowSizeSmall** <br/> |
| 2   <br/> | Mediano  <br/> |**visArrowSizeMedium** <br/> |
| 3   <br/> | Grande  <br/> |**visArrowSizeLarge** <br/> |
| 4   <br/> | Muy grande  <br/> |**visArrowSizeVeryLarge** <br/> |
| 5   <br/> | Gigantes  <br/> |**visArrowSizeJumbo** <br/> |
| 6   <br/> | Colosal  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el tamaño de la punta de flecha en el cuadro de diálogo **Línea**. 
  
Para obtener una referencia a la celda BeginArrowSize por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | BeginArrowSize  <br/> |
   
Para obtener una referencia desde un programa a la celda BeginArrowSize por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLine** <br/> |
| Índice de celda:  <br/> |**visLineBeginArrowSize** <br/> |
   

