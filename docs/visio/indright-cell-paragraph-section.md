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
ms.openlocfilehash: e6529bf41cb8fdd40371d9a663291961626afb56
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408869"
---
# <a name="indright-cell-paragraph-section"></a>Celda IndRight (Sección de párrafo)

Representa la distancia de separación que existe entre todas las líneas de texto de un párrafo y el margen derecho del bloque de texto. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría derecha permanece igual.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda IndRight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Para.IndRight[  *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda IndRight por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionParagraph** <br/> |
| Índice de fila:  <br/> |**visRowParagraph**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visIndentRight** <br/> |
   

