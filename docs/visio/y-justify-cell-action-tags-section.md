---
title: Celda Y Justify (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026937
localization_priority: Normal
ms.assetid: 27042b62-7623-95d7-7e10-f589d74605c7
description: Desplazamiento Y del botón de etiqueta de acción en relación con el punto definido por las celdas X e Y.
ms.openlocfilehash: d7a1f5c1feda3624c9f96039e7247c737a91a813
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419985"
---
# <a name="y-justify-cell-action-tags-section"></a>Celda Y Justify (sección de etiquetas de acción)

Desplazamiento  *Y*  del botón de etiqueta de acción en relación con el punto definido por las celdas X e Y. 
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Justificado arriba (predeterminado).  <br/> |**visSmartTagYJustifyTop** <br/> |
| 1   <br/> | Centrada.  <br/> |**visSmartTagYJustifyMiddle** <br/> |
| 2   <br/> | Justificado abajo.  <br/> |**visSmartTagYJustifyBottom** <br/> |
   
## <a name="remarks"></a>Comentarios

Las celdas X Justify e Y Justify determinan dónde se coloca el botón de etiqueta de acción en relación con el punto definido en las celdas X e Y.
  
Para obtener una referencia a la celda Y Justify por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | SmartTags.  *nombre*  . YJustifique donde SmartTags. *es*  el nombre de la fila de etiqueta de acción  <br/> |
   
Para obtener una referencia desde un programa a la celda Y Justify por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionSmartTag** <br/> |
| Índice de fila:  <br/> |**visRowSmartTag**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSmartTagYJustify** <br/> |
   

