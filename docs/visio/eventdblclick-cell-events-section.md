---
title: Celda EventDblClick (Sección de eventos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251312
localization_priority: Normal
ms.assetid: ca949013-f998-1bce-39e5-ac6f68ab2392
description: Una celda de evento que se evalúa cuando se hace doble clic en una forma.
ms.openlocfilehash: a50e88ecd8e432629e246f7038dfcc9626725cc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337173"
---
# <a name="eventdblclick-cell-events-section"></a>Celda EventDblClick (Sección de eventos)

Una celda de evento que se evalúa cuando se hace doble clic en una forma.
  
## <a name="remarks"></a>Comentarios

Las celdas de eventos se evalúan sólo cuando se produce el evento, no al escribir la fórmula.
  
Para obtener una referencia a la celda EventDblClick por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | EventDblClick  <br/> |
   
Para obtener una referencia desde un programa a la celda EventDblClick por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowEvent** <br/> |
| Índice de celda:  <br/> |**visEvtCellDblClick** <br/> |
   

