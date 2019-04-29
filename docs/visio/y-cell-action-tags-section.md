---
title: Celda Y (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026934
localization_priority: Normal
ms.assetid: b213fc46-7f80-99fd-60ba-8ddf3d0f6ee3
description: La posición de la coordenada y de las coordenadas locales de la forma en torno a las cuales se sitúa el botón de etiqueta de acción.
ms.openlocfilehash: 02797a849a262cb506f4617aadaccedabccdab77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430227"
---
# <a name="y-cell-action-tags-section"></a>Celda Y (sección de etiquetas de acción)

La posición de la coordenada *y* de las coordenadas locales de la forma en torno a las cuales se sitúa el botón de etiqueta de acción. 
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
## <a name="remarks"></a>Comentarios

Las celdas X e Y definen un punto en las coordenadas locales de la forma, y las celdas X Justify e Y Justify definen dónde se coloca el botón de etiqueta de acción en relación con ese punto. 
  
Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | SmartTags.  *nombre* . Y donde SmartTags. *nombre* es el nombre de la fila de la etiqueta de acción.  <br/> |
   
Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionSmartTag** <br/> |
| Índice de fila:  <br/> |**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSmartTagY** <br/> |
   

