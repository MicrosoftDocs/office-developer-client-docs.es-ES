---
title: Celda IndFirst (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251254
localization_priority: Normal
ms.assetid: 0f2e362a-3ace-787d-6326-b5bf707f0727
description: Representa la distancia de separación que existe entre la primera línea de cada párrafo en el bloque de texto y la sangría izquierda del párrafo. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría de la primera línea permanece igual.
ms.openlocfilehash: aa6d9fd14a40f4fe6b269d9750f603d8faf1d550
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410325"
---
# <a name="indfirst-cell-paragraph-section"></a>Celda IndFirst (Sección de párrafo)

Representa la distancia de separación que existe entre la primera línea de cada párrafo en el bloque de texto y la sangría izquierda del párrafo. Este valor no depende de la escala de dibujo. Si se cambia la escala, la sangría de la primera línea permanece igual.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda IndFirst por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Para.IndFirst[  *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda IndFirst por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionParagraph** <br/> |
| Índice de fila:  <br/> |**visRowParagraph**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visIndentFirst** <br/> |
   

