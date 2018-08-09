---
title: Celda SpAfter (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm960
localization_priority: Normal
ms.assetid: 2dd56ae5-300e-ba09-a73a-83c2b6c2a0ef
description: Determina el espacio insertado después de cada párrafo en el bloque de texto de la forma, además del espacio que determinen la celda SpLine y, si se trata del último párrafo de un bloque de texto, la celda BottomMargin.
ms.openlocfilehash: 93db93e58124b5f176fb57f843580eff6a3d4d3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823327"
---
# <a name="spafter-cell-paragraph-section"></a>Celda SpAfter (sección Párrafo)

Determina el espacio insertado después de cada párrafo en el bloque de texto de la forma, además del espacio que determinen la celda SpLine y, si se trata del último párrafo de un bloque de texto, la celda BottomMargin.
  
## <a name="remarks"></a>Comentarios

Este valor no depende de la escala del dibujo. Si se cambia la escala del dibujo, el espacio después del párrafo permanece igual.
  
Para obtener una referencia a la celda SpAfter por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Para.SpAfter [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda SpAfter por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionParagraph** <br/> |
| Índice de fila:  <br/> |**visRowParagraph** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSpaceAfter** <br/> |
   

