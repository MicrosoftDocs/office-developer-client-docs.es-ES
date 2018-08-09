---
title: Celda IndRight (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251256
localization_priority: Normal
ms.assetid: f0891064-95d9-ae1b-28f3-3aef1406b636
description: Representa la distancia de separación que existe entre todas las líneas de texto de un párrafo y el margen derecho del bloque de texto. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría derecha permanece igual.
ms.openlocfilehash: 83f2688e598ffb335a9fafd1eed56ea17ffd4b2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822334"
---
# <a name="indright-cell-paragraph-section"></a>Celda IndRight (sección Párrafo)

Representa la distancia de separación que existe entre todas las líneas de texto de un párrafo y el margen derecho del bloque de texto. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría derecha permanece igual.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda IndRight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Para.IndRight [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda IndRight por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionParagraph** <br/> |
| Índice de fila:  <br/> |**visRowParagraph** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visIndentRight** <br/> |
   

