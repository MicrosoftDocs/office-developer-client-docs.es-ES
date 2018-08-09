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
ms.openlocfilehash: b38e4a0685fce6d7f4aea2192ed123665eacf40a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821550"
---
# <a name="beginarrowsize-cell-line-format-section"></a>Celda BeginArrowSize (sección Formato de línea)

Determina el tamaño de la punta de flecha que aparece en la parte inicial de la línea.
  
|**Valor**|**Size**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Muy pequeño  <br/> |**visArrowSizeVerySmall** <br/> |
| 1  <br/> | Pequeño  <br/> |**visArrowSizeSmall** <br/> |
| 2  <br/> | Medio  <br/> |**visArrowSizeMedium** <br/> |
| 3  <br/> | Grande  <br/> |**visArrowSizeLarge** <br/> |
| 4  <br/> | Muy grande  <br/> |**visArrowSizeVeryLarge** <br/> |
| 5  <br/> | Enorme  <br/> |**visArrowSizeJumbo** <br/> |
| 6  <br/> | Colosal  <br/> |**visArrowSizeColossal** <br/> |
   
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
   

