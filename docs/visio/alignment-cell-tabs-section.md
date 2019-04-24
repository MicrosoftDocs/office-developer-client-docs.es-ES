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
ms.openlocfilehash: 461357c9c838fb4c0e5b0159bf027dd6adce26f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341541"
---
# <a name="alignment-cell-tabs-section"></a>Celda Alignment (Sección de tabulaciones)

Especifica la alineación de las tabulaciones.
  
|**Value**|**Alignment**|**Constante de automatización**|
|:-----|:-----|:-----|
| comprendi  <br/> | Left  <br/> |**visTabStopLeft** <br/> |
| 1  <br/> | Hacia el centro  <br/> |**visTabStopCenter** <br/> |
| segundo  <br/> | Derecha  <br/> |**visTabStopRight** <br/> |
| 3  <br/> | Decimal  <br/> |**visTabStopDecimal** <br/> |
| 4  <br/> | Coma  <br/> |**visTabStopComma** <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Alignment por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Etiquetas.  *ij* donde *i y j =* <1>, 2, 3  <br/> |
   
Para obtener una referencia a la celda Alignment por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionTab** <br/> |
| Índice de fila:  <br/> |**visRowTab +** *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> | (*j* * 3) **+ visTabAlign** <br/> |
   

