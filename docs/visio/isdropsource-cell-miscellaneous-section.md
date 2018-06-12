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
ms.openlocfilehash: f2edfcb7cf9d21b2ecd97b335b07f30233903d5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822355"
---
# <a name="isdropsource-cell-miscellaneous-section"></a>Celda IsDropSource (Sección de varios)

Determina si se puede agregar una forma a un grupo soltándola en él.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Se puede agregar una forma a un grupo soltándola e él.  <br/> |
|FALSE  <br/> |No se puede agregar una forma a un grupo.  <br/> |
   
## <a name="remarks"></a>Observaciones

También puede establecer este valor mediante la selección de la forma, haciendo clic en **comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, selecciona la casilla de verificación **Agregar formas a grupos en el buzón** . 
  
Además de habilitar este comportamiento para una forma, también debe habilitar un grupo Aceptar formas que se arrastran en él. Para ello, seleccione el grupo, haga clic en **comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, seleccione la casilla de verificación **Aceptar formas colocadas** . Este valor se almacena en la celda IsDropTarget, en la sección Propiedades del grupo. 
  
Para obtener una referencia a la celda IsDropSource por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |IsDropSource  <br/> |
   
Para obtener una referencia a la celda IsDropSource por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowMisc** <br/> |
|Índice de celda:  <br/> |**visDropSource** <br/> |
   

