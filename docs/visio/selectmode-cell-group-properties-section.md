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
ms.openlocfilehash: 82f9e2806d1131a0acfd064f585c681fef0f209f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435365"
---
# <a name="selectmode-cell-group-properties-section"></a>Celda SelectMode (sección de propiedades de grupo)

Determina cómo se selecciona una forma de grupo y sus miembros.
  
|**Valor**|**Modo de selección**|**Constante de automatización**|
|:-----|:-----|:-----|
|comprendi  <br/> |Se selecciona sólo la forma de grupo.  <br/> |**visGrpSelModeGroupOnly** <br/> |
|1  <br/> |Se selecciona primero la forma de grupo.  <br/> |**visGrpSelModeGroup1st** <br/> |
|segundo  <br/> |Se seleccionan primero los miembros del grupo.  <br/> |**visGrpSelModeMembers1st** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer este valor en el cuadro de diálogo **comportamiento** (seleccione la forma de grupo, en la ficha [programador](run-in-developer-mode-display-the-developer-tab.md) , en el grupo **diseño de formas** , haga clic en **comportamiento**y, a continuación, haga clic en un modo de la lista **selección** debajo de **Grupo Comportamiento** ). 
  
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
   

