---
title: Celda DisplayMode (sección Etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: Determina si la etiqueta de acción aparece cuando el usuario mueve el puntero sobre la etiqueta, cuando se selecciona la forma o todo el tiempo.
ms.openlocfilehash: 4cb0666ca8de28247309de4fc0d2ff23e8b37d8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821973"
---
# <a name="displaymode-cell-action-tags-section"></a>Celda DisplayMode (sección Etiquetas de acción)

Determina si la etiqueta de acción aparece cuando el usuario mueve el puntero sobre la etiqueta, cuando se selecciona la forma o todo el tiempo.
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
|**Valor**|**Modo de presentación**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Aparece cuando se sitúa el puntero sobre la etiqueta (valor predeterminado).  <br/> |**visSmartTagDispModeMouseOver** <br/> |
| 1  <br/> | Aparece mientras está seleccionada la forma.  <br/> |**visSmartTagDispModeShapeSelected** <br/> |
| 2  <br/> | Aparece siempre.  <br/> |**visSmartTagDispModeAlways** <br/> |
   
## <a name="remarks"></a>Comentarios

Las etiquetas de acción no aparecen en las versiones impresas ni en las publicaciones. 
  
Si se define una etiqueta de acción para una página y esta celda contiene el valor 1, la etiqueta no aparecerá nunca, ya que no se puede seleccionar una página. 
  
Para obtener una referencia a la celda DisplayMode por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Etiquetas inteligentes.  *nombre* . DisplayMode donde SmartTags. *nombre* es el nombre de la fila de etiquetas de acción  <br/> |
   
Para obtener una referencia desde un programa a la celda DisplayMode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionSmartTag** <br/> |
| Índice de fila:  <br/> |**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSmartTagDisplayMode** <br/> |
   

