---
title: Celda X Justify (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
localization_priority: Normal
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: La - desplazamiento x del botón de etiqueta de acción en relación con el punto definido por las celdas X e Y.
ms.openlocfilehash: 043d7b198ae5a529c623545fb54ef5aa1d32217d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823566"
---
# <a name="x-justify-cell-action-tags-section"></a>Celda X Justify (sección de etiquetas de acción)

La *x* -desplazamiento del botón de etiqueta de acción en relación con el punto definido por las celdas X e Y. 
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Justificado a la izquierda (predeterminado).  <br/> |**visSmartTagXJustifyLeft** <br/> |
| 1  <br/> | Centrada.  <br/> |**visSmartTagXJustifyCenter** <br/> |
| 2  <br/> | Justificado a la derecha.  <br/> |**visSmartTagXJustifyRight** <br/> |
   
## <a name="remarks"></a>Notas

Las celdas X Justify e Y Justify determinan dónde se coloca el botón de etiqueta de acción en relación con el punto definido en las celdas X e Y. 
  
Para obtener una referencia a la celda X Justify por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Etiquetas inteligentes.  *nombre* . XJustify donde SmartTags. *nombre* es el nombre de la fila de etiquetas de acción  <br/> |
   
Para obtener una referencia a la celda X Justify por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionSmartTag** <br/> |
| Índice de fila:  <br/> |**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSmartTagXJustify** <br/> |
   

