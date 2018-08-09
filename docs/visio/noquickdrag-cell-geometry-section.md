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
description: Determina si una forma se puede seleccionar o arrastrar cuando el usuario hace clic en el área con relleno definido por la sección de geometría.
ms.openlocfilehash: 7d4ffd876d8676af885b8f750fecf6f6d0deaa9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822686"
---
# <a name="noquickdrag-cell-geometry-section"></a>Celda NoQuickDrag (sección Geometría)

Determina si una forma se puede seleccionar o arrastrar cuando el usuario hace clic en el área con relleno definido por la sección de geometría.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda NoQuickDrag por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Geometría *i* . NoQuickDrag, donde * i * - < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda NoQuickDrag por su índice, use la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionFirstComponent** +  *i* , donde *i* = 0, 1, 2...  <br/> |
|Índice de fila:  <br/> |**visRowComponent** <br/> |
|Índice de celda:  <br/> |**visCompNoQuickDrag** <br/> |
   

