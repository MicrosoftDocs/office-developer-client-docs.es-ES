---
title: Celda EventDrop (Sección de eventos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm350
localization_priority: Normal
ms.assetid: f84afe83-8391-0c13-f442-ea8794b38642
description: Una celda de evento que se evalúa cuando se coloca una forma en la página de dibujo, ya sea como una instancia o al duplicar o pegar la forma.
ms.openlocfilehash: f1433394dbd58c7c4422c6bca1e79a4f2c8e0c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408596"
---
# <a name="eventdrop-cell-events-section"></a>Celda EventDrop (Sección de eventos)

Una celda de evento que se evalúa cuando se coloca una forma en la página de dibujo, ya sea como una instancia o al duplicar o pegar la forma.
  
## <a name="remarks"></a>Comentarios

Las celdas de eventos se evalúan sólo cuando se produce el evento, no al escribir la fórmula.
  
Para obtener una referencia a la celda EventDrop por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | EventDrop  <br/> |
   
Para obtener una referencia desde un programa a la celda EventDrop por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowEvent** <br/> |
| Índice de celda:  <br/> |**visEvtCellDrop** <br/> |
   

