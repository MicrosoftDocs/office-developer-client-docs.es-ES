---
title: Celda EventMultiDrop (Sección de eventos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: caa86e33d0d7aa9ca31cbbf8939e17b581877669
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337194"
---
# <a name="eventmultidrop-cell-events-section"></a>Celda EventMultiDrop (Sección de eventos)

Una celda de evento que se evalúa cuando se colocan varias formas en la página de dibujo, ya sea como instancias o cuando se duplican o se pegan formas.
  
Las celdas de eventos se evalúan sólo cuando se produce el evento, no al escribir la fórmula.
  
Para hacer referencia a la celda EventMultiDrop por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |EventMultiDrop  <br/> |
   
Para hacer referencia desde un programa a la celda EventMultiDrop según su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowEvent** <br/> |
|Índice de celda:  <br/> |**visEvtCellMultiDrop** <br/> |
   

