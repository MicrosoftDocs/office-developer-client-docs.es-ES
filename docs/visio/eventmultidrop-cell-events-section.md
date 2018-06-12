---
title: Celda EventMultiDrop (Sección de eventos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: e44cd18c3f7673761f457db9cd4bfe00a8ab89bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822092"
---
# <a name="eventmultidrop-cell-events-section"></a>Celda EventMultiDrop (Sección de eventos)

Una celda de evento que se evalúa cuando se colocan varias formas en la página de dibujo, como instancias o cuando se duplicar o pegar formas.
  
Las celdas de eventos se evalúan sólo cuando se produce el evento, no al escribir la fórmula.
  
Para hacer referencia a la celda EventMultiDrop por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |EventMultiDrop  <br/> |
   
Para hacer referencia a la celda EventMultiDrop por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowEvent** <br/> |
|Índice de celda:  <br/> |**visEvtCellMultiDrop** <br/> |
   

