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
ms.openlocfilehash: 942ccee4478c87243207d8d65785857758d2a068
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823402"
---
# <a name="thetext-cell-events-section"></a>Celda TheText (sección Eventos)

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
   

