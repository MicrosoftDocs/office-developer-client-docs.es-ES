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
description: Desplazamiento y del botón de etiqueta de acción en relación con el punto definido por las celdas X e y.
ms.openlocfilehash: d7a1f5c1feda3624c9f96039e7247c737a91a813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357018"
---
# <a name="y-justify-cell-action-tags-section"></a>Celda Y Justify (sección de etiquetas de acción)

Desplazamiento *y* del botón de etiqueta de acción en relación con el punto definido por las celdas X e y. 
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
|**Value**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| comprendi  <br/> | Justificado arriba (predeterminado).  <br/> |**visSmartTagYJustifyTop** <br/> |
| 1  <br/> | Centrada.  <br/> |**visSmartTagYJustifyMiddle** <br/> |
| segundo  <br/> | Justificado abajo.  <br/> |**visSmartTagYJustifyBottom** <br/> |
   
## <a name="remarks"></a>Comentarios

Las celdas X Justify e y Justify determinan dónde se coloca el botón de etiqueta de acción en relación con el punto definido en las celdas X e y.
  
Para obtener una referencia a la celda Y Justify por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | SmartTags.  *nombre* . YJustify donde SmartTags. *nombre* es el nombre de la fila de la etiqueta de acción.  <br/> |
   
Para obtener una referencia desde un programa a la celda Y Justify por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionSmartTag** <br/> |
| Índice de fila:  <br/> |**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSmartTagYJustify** <br/> |
   

