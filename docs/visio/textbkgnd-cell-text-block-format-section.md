---
title: Celda TextBkgnd (Sección de formato del bloque de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251267
localization_priority: Normal
ms.assetid: a238bf1c-1acd-eacd-22f3-a48acaaa4549
description: Determina el color de fondo del texto de una forma.
ms.openlocfilehash: 2450bf0cb0e013c0f9310eacfca0f5a20e7e6063
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406545"
---
# <a name="textbkgnd-cell-text-block-format-section"></a>Celda TextBkgnd (Sección de formato del bloque de texto)

Determina el color de fondo del texto de una forma.
  
## <a name="remarks"></a>Comentarios

La celda TextBkgnd puede tener cualquier valor entre 0 y 24, o 255. Los valores 0 y 255 ( *visTxtBlklOpaque*) indican un fondo de texto transparente. 
  
Para especificar un color personalizado, utilice la función RGB o HSL más uno; por ejemplo, RGB(255,127,255)+1. El valor de un color personalizado es su color RGB y RGB( *r, g, b*)+1, en lugar de un número, se mostrará en la ventana ShapeSheet. Cuando se utilizan en operaciones numéricas, los colores personalizados tienen valores iguales o mayores que 25. 
  
Puede establecer la transparencia del color de fondo del texto en la celda TextBkgndTrans.
  
Para obtener una referencia a la celda TextBkgnd por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |TextBkgnd  <br/> |
   
Para obtener una referencia desde un programa a la celda TextBkgnd por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowText** <br/> |
|Índice de celda:  <br/> |**visTxtBlkBkgnd** <br/> |
   

