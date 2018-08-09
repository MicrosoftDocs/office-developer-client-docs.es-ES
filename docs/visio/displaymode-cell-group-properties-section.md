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
ms.openlocfilehash: 086685b47d8eaf170a8722f7cd00545230541e79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821985"
---
# <a name="displaymode-cell-group-properties-section"></a>Celda DisplayMode (sección Propiedades de grupo)

Determina cómo se muestran la forma de grupo y sus miembros.
  
|**Valor**|**Modo de presentación**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Oculta la forma de grupo y el texto.  <br/> |**visGrpDispModeNone** <br/> |
|1  <br/> |Muestra la forma de grupo detrás de las formas pertenecientes.  <br/> |**visGrpDispModeBack** <br/> |
|2  <br/> |Muestra la forma de grupo delante de las formas pertenecientes.  <br/> |**visGrpDispModeFront** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer este valor seleccionar el grupo, haciendo clic en **comportamiento** en el grupo **Diseño de formas** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, seleccionar un modo de presentación de la lista de **datos de grupo** . 
  
Para obtener una referencia a la celda DisplayMode por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |DisplayMode  <br/> |
   
Para obtener una referencia desde un programa a la celda DisplayMode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowGroup** <br/> |
|Índice de celda:  <br/> |**visGroupDisplayMode** <br/> |
   

