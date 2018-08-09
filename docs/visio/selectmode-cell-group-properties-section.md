---
title: Celda SelectMode (Sección de propiedades de grupo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm875
localization_priority: Normal
ms.assetid: 5ba68e05-f394-d7b7-390d-f0a9fdad011e
description: Determina cómo se selecciona una forma de grupo y sus miembros.
ms.openlocfilehash: 426b4a18bbd54887e4f60b92860a6c3846386671
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823117"
---
# <a name="selectmode-cell-group-properties-section"></a>Celda SelectMode (sección Propiedades de grupo)

Determina cómo se selecciona una forma de grupo y sus miembros.
  
|**Valor**|**Modo de selección**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Se selecciona sólo la forma de grupo.  <br/> |**visGrpSelModeGroupOnly** <br/> |
|1  <br/> |Se selecciona primero la forma de grupo.  <br/> |**visGrpSelModeGroup1st** <br/> |
|2  <br/> |Se seleccionan primero los miembros del grupo.  <br/> |**visGrpSelModeMembers1st** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer este valor en el cuadro de diálogo **comportamiento** (con la forma de grupo, en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) , en el grupo **Diseño de formas** , haga clic en **comportamiento**y, a continuación, haga clic en un modo en la lista de **selección** en **grupo Comportamiento de** ). 
  
Para obtener una referencia a la celda SelectMode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |SelectMode  <br/> |
   
Para obtener una referencia desde un programa a la celda SelectMode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowGroup** <br/> |
|Índice de celda:  <br/> |**visGroupSelectMode** <br/> |
   

