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
ms.openlocfilehash: d33a10220499020ba1a1acedf5782fdb78925c07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823304"
---
# <a name="spbefore-cell-paragraph-section"></a>Celda SpBefore (sección Párrafo)

Determina el espacio insertado antes de cada párrafo en el bloque de texto de la forma, además del espacio que determinen la celda SpLine y, si se trata del primer párrafo de un bloque de texto, la celda TopMargin.
  
## <a name="remarks"></a>Comentarios

Este valor no depende de la escala del dibujo. Si se cambia la escala del dibujo, el espacio delante del párrafo permanece igual.
  
Para obtener una referencia a la celda SpBefore por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Para.SpBefore [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda SpBefore por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionParagraph** <br/> |
| Índice de fila:  <br/> |**visRowParagraph** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSpaceBefore** <br/> |
   

