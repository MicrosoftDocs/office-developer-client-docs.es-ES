---
title: Celda EventXFMod (Sección de eventos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251313
localization_priority: Normal
ms.assetid: b88588a2-c651-7eab-9c7a-ed78f20d1ba3
description: Una celda de evento que se evalúa cuando se transforma la posición o la orientación de una forma en la página (XF).
ms.openlocfilehash: c4ed4ddd9b255a9a52fc81349b514dbd25772c98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418536"
---
# <a name="eventxfmod-cell-events-section"></a>Celda EventXFMod (Sección de eventos)

Una celda de evento que se evalúa cuando se transforma ("XF") la posición u orientación de la página.
  
## <a name="remarks"></a>Comentarios

Las celdas de eventos se evalúan sólo cuando se produce el evento, no al escribir la fórmula.
  
Para obtener una referencia a la celda EventXFMod por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | EventXFMod  <br/> |
   
Para obtener una referencia desde un programa a la celda EventXFMod por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowEvent** <br/> |
| Índice de celda:  <br/> |**visEvtCellXFMod** <br/> |
   

