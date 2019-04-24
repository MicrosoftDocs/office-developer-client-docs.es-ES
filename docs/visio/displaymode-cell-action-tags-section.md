---
title: Celda DisplayMode (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: Determina si la etiqueta de acción aparece cuando el usuario mueve el puntero sobre la etiqueta, cuando se selecciona la forma o siempre.
ms.openlocfilehash: 0254ad361c63dfdeddaf8a1c2173e99aa1c05398
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332735"
---
# <a name="displaymode-cell-action-tags-section"></a>Celda DisplayMode (sección de etiquetas de acción)

Determina si la etiqueta de acción aparece cuando el usuario mueve el puntero sobre la etiqueta, cuando se selecciona la forma o siempre.
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
|**Value**|**Modo de presentación**|**Constante de automatización**|
|:-----|:-----|:-----|
| comprendi  <br/> | Aparece cuando se pausa el mouse sobre la etiqueta (valor predeterminado).  <br/> |**visSmartTagDispModeMouseOver** <br/> |
| 1  <br/> | Aparece mientras está seleccionada la forma.  <br/> |**visSmartTagDispModeShapeSelected** <br/> |
| segundo  <br/> | Aparece siempre.  <br/> |**visSmartTagDispModeAlways** <br/> |
   
## <a name="remarks"></a>Comentarios

Las etiquetas de acción no aparecen en las versiones impresas ni en las publicaciones. 
  
Si se define una etiqueta de acción para una página y esta celda contiene el valor 1, la etiqueta no aparecerá nunca, ya que no se puede seleccionar una página. 
  
Para obtener una referencia a la celda DisplayMode por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | SmartTags.  *nombre* . DisplayMode donde SmartTags. *nombre* es el nombre de la fila de la etiqueta de acción.  <br/> |
   
Para obtener una referencia a la celda DisplayMode por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionSmartTag** <br/> |
| Índice de fila:  <br/> |**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSmartTagDisplayMode** <br/> |
   

