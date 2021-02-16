---
title: Celda X (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60093
localization_priority: Normal
ms.assetid: d13e362b-9b69-30c5-003a-9c5df2aa29f6
description: Posición de coordenada x en las coordenadas locales de la forma alrededor de la cual se coloca el botón de etiqueta de acción.
ms.openlocfilehash: 9f26bec81563c9813a88ed5c69730266834ee101
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431116"
---
# <a name="x-cell-action-tags-section"></a>Celda X (sección de etiquetas de acción)

Posición de coordenada  *x*  en las coordenadas locales de la forma alrededor de la cual se coloca el botón de etiqueta de acción. 
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
## <a name="remarks"></a>Comentarios

Las celdas X e Y definen un punto en las coordenadas locales de la forma, y las celdas X Justify e Y Justify definen dónde se coloca el botón de etiqueta de acción en relación con ese punto. 
  
Para obtener una referencia a la celda X por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> |SmartTags. *nombre*  . X donde SmartTags. *es*  el nombre de la fila de etiqueta de acción  <br/> |
   
Para obtener una referencia desde un programa a la celda X por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionSmartTag** <br/> |
| Índice de fila:  <br/> |**visRowSmartTag**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSmartTagX** <br/> |
   

