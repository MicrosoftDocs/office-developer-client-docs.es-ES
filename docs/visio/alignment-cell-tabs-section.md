---
title: Celda Alignment (Sección de tabulaciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
localization_priority: Normal
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: Especifica la alineación de las tabulaciones.
ms.openlocfilehash: a2178c63d0005ee8b2f0c8ebcfbc25854a5b1567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821516"
---
# <a name="alignment-cell-tabs-section"></a>Celda Alignment (sección Tabulaciones)

Especifica la alineación de las tabulaciones.
  
|**Valor**|**Alineación**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Izquierda  <br/> |**visTabStopLeft** <br/> |
| 1  <br/> | Centro  <br/> |**visTabStopCenter** <br/> |
| 2  <br/> | Derecha  <br/> |**visTabStopRight** <br/> |
| 3  <br/> | Decimal  <br/> |**visTabStopDecimal** <br/> |
| 4  <br/> | Coma  <br/> |**visTabStopComma** <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Alignment por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Fichas.  *ij* donde *i y j =* < 1 >, 2, 3  <br/> |
   
Para obtener una referencia a la celda Alignment por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionTab** <br/> |
| Índice de fila:  <br/> |**visRowTab +** *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> | (*j* * 3) **+ visTabAlign** <br/> |
   

