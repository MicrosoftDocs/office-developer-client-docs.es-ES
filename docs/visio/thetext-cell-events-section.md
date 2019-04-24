---
title: Celda TheText (Sección de eventos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1005
localization_priority: Normal
ms.assetid: 2d63768e-afdb-4b3f-de49-f9ba69ae5391
description: Celda de evento que se evalúa cuando cambia el texto o la composición del texto de una forma.
ms.openlocfilehash: 6aa5e14f339d0030d8421eaae62b0e481be91fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326680"
---
# <a name="thetext-cell-events-section"></a>Celda TheText (Sección de eventos)

Celda de evento que se evalúa cuando cambia el texto o la composición del texto de una forma.
  
## <a name="remarks"></a>Comentarios

Las celdas de eventos se evalúan sólo cuando se produce el evento, no al escribir la fórmula. Puede utilizar la celda TheText para activar cálculos, por ejemplo, para volver a calcular el ancho y el alto del texto con las funciones TEXTWIDTH( ) y TEXTHEIGHT( ).
  
Para obtener una referencia a la celda TheText por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | TheText  <br/> |
   
Para obtener una referencia desde un programa a la celda TheText por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowEvent** <br/> |
| Índice de celda:  <br/> |**visEvtCellTheText** <br/> |
   

