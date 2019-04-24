---
title: Celda IsTextEditTarget (Sección de propiedades de grupo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
localization_priority: Normal
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: Determina las asignaciones de texto para un grupo.
ms.openlocfilehash: 78a70dc0398745765bca12a1e768390b35fce8ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314920"
---
# <a name="istextedittarget-cell-group-properties-section"></a>Celda IsTextEditTarget (Sección de propiedades de grupo)

Determina las asignaciones de texto para un grupo.
  
|**Value**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El texto se agrega a la forma del grupo.  <br/> |
|FALSE  <br/> |El texto se agrega a la forma en el grupo en la parte superior del orden de apilamiento.  <br/> |
   
## <a name="remarks"></a>Comentarios

También puede ajustar este valor si selecciona un grupo, hace clic en **Comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, activa la casilla **Modificar el texto del grupo**. 
  
Los grupos creados con versiones anteriores a Visio 2000 tienen el valor predeterminado FALSE. A partir de la versión 2000 de Visio, el valor predeterminado es TRUE. 
  
Para obtener una referencia a la celda IsTextEditTarget por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |IsTextEditTarget  <br/> |
   
Para obtener una referencia desde un programa a la celda IsTextEditTarget por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowGroup** <br/> |
|Índice de celda:  <br/> |**visGroupIsTextEditTarget** <br/> |
   

