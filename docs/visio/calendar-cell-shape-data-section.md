---
title: Celda Calendar (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60027
localization_priority: Normal
ms.assetid: f5dcc6d9-474a-9ecb-21f5-56415d934890
description: Determina el calendario que se usa para los datos de formas cuando el tipo de datos es Date.
ms.openlocfilehash: 2ddbd578053e2ae37514194450bd95dc9cdf441d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432761"
---
# <a name="calendar-cell-shape-data-section"></a>Celda Calendar (Sección de datos de formas)

Determina el calendario que se usa para los datos de formas cuando el tipo de datos es Date.
  
## <a name="remarks"></a>Comentarios

Los valores posibles son: 0 (Occidental), 1 (Hijri árabe), 2 (Hebreo lunar), 3 (Calendario de Taiwán), 4 (Japonés imperial), 5 (Budista tailandés), 6 (Danki coreano), 7 (Saka), 8 (Transliteración al inglés) y 9 (Transliteración al francés). 
  
Para obtener una referencia a la celda Calendar por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Prop.  *nombre*  . Calendario donde Prop.  *nombre*  es el nombre de fila  <br/> |
   
Para obtener una referencia desde un programa a la celda Calendar por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionProp** <br/> |
| Índice de fila:  <br/> |**visRowProp**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCustPropsCalendar** <br/> |
   

