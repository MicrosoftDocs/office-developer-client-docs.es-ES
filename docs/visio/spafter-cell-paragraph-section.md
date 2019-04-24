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
ms.openlocfilehash: 2b8fe7e2b0df09561d0db4367f917c8f4b71335d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335227"
---
# <a name="spafter-cell-paragraph-section"></a>Celda SpAfter (Sección de párrafo)

Determina el espacio insertado después de cada párrafo en el bloque de texto de la forma, además del espacio que determinen la celda SpLine y, si se trata del último párrafo de un bloque de texto, la celda BottomMargin.
  
## <a name="remarks"></a>Comentarios

Este valor no depende de la escala del dibujo. Si se cambia la escala del dibujo, el espacio después del párrafo permanece igual.
  
Para obtener una referencia a la celda SpAfter por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Para. SpAfter [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda SpAfter por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionParagraph** <br/> |
| Índice de fila:  <br/> |**visRowParagraph** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSpaceAfter** <br/> |
   

