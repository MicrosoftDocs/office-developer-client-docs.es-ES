---
title: Celda SpBefore (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm965
localization_priority: Normal
ms.assetid: a7d5b0a1-3657-8211-f0e0-eaed588fa0bc
description: Determina el espacio insertado antes de cada párrafo en el bloque de texto de la forma, además del espacio que determinen la celda SpLine y, si se trata del primer párrafo de un bloque de texto, la celda TopMargin.
ms.openlocfilehash: 9890910a11990bb5be7fe3ee4af95e578c8d9799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425760"
---
# <a name="spbefore-cell-paragraph-section"></a>Celda SpBefore (Sección de párrafo)

Determina el espacio insertado antes de cada párrafo en el bloque de texto de la forma, además del espacio que determinen la celda SpLine y, si se trata del primer párrafo de un bloque de texto, la celda TopMargin.
  
## <a name="remarks"></a>Comentarios

Este valor no depende de la escala del dibujo. Si se cambia la escala del dibujo, el espacio delante del párrafo permanece igual.
  
Para obtener una referencia a la celda SpBefore por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Para. SpBefore [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda SpBefore por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionParagraph** <br/> |
| Índice de fila:  <br/> |**visRowParagraph** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSpaceBefore** <br/> |
   

