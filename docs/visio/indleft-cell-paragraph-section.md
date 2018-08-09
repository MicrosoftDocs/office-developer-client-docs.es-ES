---
title: Celda IndLeft (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251255
localization_priority: Normal
ms.assetid: 31a7d0d4-4666-ddef-c5eb-4d13803e6a2f
description: Representa la distancia de separación que existe entre todas las líneas de texto de un párrafo y el margen izquierdo del bloque de texto. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría izquierda permanece igual.
ms.openlocfilehash: 2ccccfdeacc73539c612790613c7eca85de55b34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822332"
---
# <a name="indleft-cell-paragraph-section"></a>Celda IndLeft (sección Párrafo)

Representa la distancia de separación que existe entre todas las líneas de texto de un párrafo y el margen izquierdo del bloque de texto. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría izquierda permanece igual.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda IndLeft por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Para.IndLeft [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda IndLeft por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionParagraph** <br/> |
| Índice de fila:  <br/> |**visRowParagraph** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visIndentLeft** <br/> |
   

