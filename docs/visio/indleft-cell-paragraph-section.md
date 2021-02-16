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
ms.openlocfilehash: 2a942ef3d874b8d1ce2ef85f423c93bc0db33230
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405166"
---
# <a name="indleft-cell-paragraph-section"></a>Celda IndLeft (Sección de párrafo)

Representa la distancia de separación que existe entre todas las líneas de texto de un párrafo y el margen izquierdo del bloque de texto. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría izquierda permanece igual.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda IndLeft por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Para.IndLeft[  *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda IndLeft por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionParagraph** <br/> |
| Índice de fila:  <br/> |**visRowParagraph**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visIndentLeft** <br/> |
   

