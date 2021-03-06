---
title: Celda NoQuickDrag (sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
localization_priority: Normal
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: Determina si se puede seleccionar o arrastrar una forma cuando el usuario hace clic en el área rellenada definida por la sección Geometría.
ms.openlocfilehash: d60268685d93ae88abb2840f62b093db1e688c2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417724"
---
# <a name="noquickdrag-cell-geometry-section"></a>Celda NoQuickDrag (sección de geometría)

Determina si se puede seleccionar o arrastrar una forma cuando el usuario hace clic en el área rellenada definida por la sección Geometría.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda NoQuickDrag por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Geometría  *i*  . NoQuickDrag, donde * i * - <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda NoQuickDrag por su índice, use la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionFirstComponent**  +   *i* , donde *i* = 0, 1, 2...  <br/> |
|Índice de fila:  <br/> |**visRowComponent** <br/> |
|Índice de celda:  <br/> |**visCompNoQuickDrag** <br/> |
   

