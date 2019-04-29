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
description: Desplazamiento x del botón de etiqueta de acción en relación con el punto definido por las celdas X e y.
ms.openlocfilehash: f8542d2f3a22b12794d999323d202d7a5bece20b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414126"
---
# <a name="x-justify-cell-action-tags-section"></a>Celda X Justify (sección de etiquetas de acción)

Desplazamiento *x* del botón de etiqueta de acción en relación con el punto definido por las celdas x e y. 
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| comprendi  <br/> | Justificado a la izquierda (predeterminado).  <br/> |**visSmartTagXJustifyLeft** <br/> |
| 1  <br/> | Centrada.  <br/> |**visSmartTagXJustifyCenter** <br/> |
| segundo  <br/> | Justificado a la derecha.  <br/> |**visSmartTagXJustifyRight** <br/> |
   
## <a name="remarks"></a>Comentarios

Las celdas X Justify e y Justify determinan dónde se coloca el botón de etiqueta de acción en relación con el punto definido en las celdas X e y. 
  
Para obtener una referencia a la celda X Justify por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | SmartTags.  *nombre* . XJustify donde SmartTags. *nombre* es el nombre de la fila de la etiqueta de acción.  <br/> |
   
Para obtener una referencia desde un programa a la celda X Justify por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionSmartTag** <br/> |
| Índice de fila:  <br/> |**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSmartTagXJustify** <br/> |
   

