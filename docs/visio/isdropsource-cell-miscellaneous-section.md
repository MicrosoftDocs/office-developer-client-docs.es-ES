---
title: Celda IsDropSource (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm490
localization_priority: Normal
ms.assetid: 3b20e6ef-f1ac-5bb0-5ac3-4df3ae5e9bf9
description: Determina si se puede agregar una forma a un grupo soltándola en él.
ms.openlocfilehash: e8cb02a66f745530f12c7c8be56b9bdd771121b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421896"
---
# <a name="isdropsource-cell-miscellaneous-section"></a>Celda IsDropSource (Sección de varios)

Determina si se puede agregar una forma a un grupo soltándola en él.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Se puede agregar una forma a un grupo soltándola e él.  <br/> |
|FALSE  <br/> |No se puede agregar una forma a un grupo.  <br/> |
   
## <a name="remarks"></a>Comentarios

También puede ajustar este valor si selecciona la forma, hace clic en **Comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, selecciona la casilla **Agregar formas a un grupo al colocarlas**. 
  
Además de habilitar este comportamiento para una forma, debe habilitar también un grupo donde se puedan soltar las formas. Para ello, seleccione el grupo, haga clic en **Comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, active la casilla **Aceptar formas colocadas**. Este valor se almacena en la celda IsDropTarget, en la sección de propiedades del grupo. 
  
Para obtener una referencia a la celda IsDropSource por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |IsDropSource  <br/> |
   
Para obtener una referencia desde un programa a la celda IsDropSource por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowMisc** <br/> |
|Índice de celda:  <br/> |**visDropSource** <br/> |
   

