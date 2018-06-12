---
title: Celda Calendar (Sección de campos de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60029
localization_priority: Normal
ms.assetid: 0c3e275e-25f0-3681-03f4-257145c19690
description: Determina el calendario que se usa para un campo de texto cuando el tipo de datos es fecha.
ms.openlocfilehash: 6d9d3ef0addb1d6081e2046ca7a5a663eb2a9c8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821679"
---
# <a name="calendar-cell-text-fields-section"></a>Celda Calendar (Sección de campos de texto)

Determina el calendario que se usa para un campo de texto cuando el tipo de datos es fecha.
  
## <a name="remarks"></a>Comentarios

Los valores posibles son: 0 (Occidental), 1 (Hijri árabe), 2 (Hebreo lunar), 3 (Calendario de Taiwán), 4 (Japonés imperial), 5 (Budista tailandés), 6 (Danki coreano), 7 (Saka), 8 (Transliteración al inglés) y 9 (Transliteración al francés). 
  
Para obtener una referencia a la celda Calendar por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Fields.Calendar [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia a la celda Calendar por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionTextField** <br/> |
| Índice de fila:  <br/> |**visRowField** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visFieldCalendar** <br/> |
   

