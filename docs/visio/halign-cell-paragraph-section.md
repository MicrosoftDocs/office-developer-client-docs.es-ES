---
title: Celda HAlign (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm425
localization_priority: Normal
ms.assetid: a8d6b622-60b3-e43f-b6a1-55db561204ed
description: Determina la alineación horizontal de los caracteres del bloque de texto de una forma.
ms.openlocfilehash: a48619e2531c0a69ad63af3b88ae9f019019b1fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360182"
---
# <a name="halign-cell-paragraph-section"></a>Celda HAlign (Sección de párrafo)

Determina la alineación horizontal de los caracteres del bloque de texto de una forma.
  
|**Value**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| comprendi  <br/> | Alinear a la izquierda  <br/> |**visHorzLeft** <br/> |
| 1  <br/> | Hacia el centro  <br/> |**visHorzCenter** <br/> |
| segundo  <br/> | Alinear a la derecha  <br/> |**visHorzRight** <br/> |
| 3  <br/> | Justify  <br/> |**visHorzJustify** <br/> |
| 4  <br/> | Forzar justificar  <br/> |**visHorzForce** <br/> |
   
## <a name="remarks"></a>Comentarios

La justificación agrega espacios entre palabras en todas las líneas excepto en la última del párrafo para alinear el lado izquierdo y derecho del texto con los márgenes.
  
La opción Forzar justificación justifica todas las líneas del párrafo, incluso la última.
  
Para obtener una referencia a la celda HAlign por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Para. HorzAlign [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda HAlign por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionParagraph** <br/> |
| Índice de fila:  <br/> |**visRowParagraph** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visHorzAlign** <br/> |
   

