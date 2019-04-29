---
title: Celda DisplayMode (Sección de propiedades del grupo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
localization_priority: Normal
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: Determina cómo se muestran la forma de grupo y sus miembros.
ms.openlocfilehash: a49d7a38eac75a2845de0ca3ad22f7cbf79a63df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413188"
---
# <a name="displaymode-cell-group-properties-section"></a>Celda DisplayMode (Sección de propiedades del grupo)

Determina cómo se muestran la forma de grupo y sus miembros.
  
|**Valor**|**Modo de presentación**|**Constante de automatización**|
|:-----|:-----|:-----|
|comprendi  <br/> |Oculta la forma de grupo y el texto.  <br/> |**visGrpDispModeNone** <br/> |
|1  <br/> |Muestra la forma de grupo detrás de las formas pertenecientes.  <br/> |**visGrpDispModeBack** <br/> |
|segundo  <br/> |Muestra la forma de grupo delante de las formas pertenecientes.  <br/> |**visGrpDispModeFront** <br/> |
   
## <a name="remarks"></a>Comentarios

Para establecer este valor, también puede seleccionar el grupo, hacer clic en **comportamiento** en el grupo **diseño de formas** en la ficha [programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, seleccionar un modo de presentación de la lista **datos del grupo** . 
  
Para obtener una referencia a la celda DisplayMode por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |DisplayMode  <br/> |
   
Para obtener una referencia a la celda DisplayMode por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowGroup** <br/> |
|Índice de celda:  <br/> |**visGroupDisplayMode** <br/> |
   

