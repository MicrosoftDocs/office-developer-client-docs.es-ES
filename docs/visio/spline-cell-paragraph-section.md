---
title: Celda SpLine (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm970
localization_priority: Normal
ms.assetid: 84f4e5f1-7c28-9e83-8644-28d117bb10a5
description: Determina la distancia entre una línea de texto y la siguiente, expresada como un porcentaje, donde 100% es el alto de una línea de texto.
ms.openlocfilehash: 82b2604a62608c0cc4333892d678b1eb886a9c7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434917"
---
# <a name="spline-cell-paragraph-section"></a>Celda SpLine (Sección de párrafo)

Determina la distancia entre una línea de texto y la siguiente, expresada como un porcentaje, donde 100% es el alto de una línea de texto.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| \>comprendi  <br/> | Espaciado absoluto, independiente del tamaño de la fuente  <br/> |
| = 0  <br/> | Se establece como sólido (espaciado = 100% del tamaño de la fuente)  <br/> |
| \<comprendi  <br/> | Un porcentaje del tamaño de la fuente (por ejemplo, -120% produce un espaciado del 120%)  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda SpLine por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | 5.5. SpLine [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda SpLine por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionParagraph** <br/> |
| Índice de fila:  <br/> |**visRowParagraph** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSpaceLine** <br/> |
   

