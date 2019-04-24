---
title: Celda Name (Sección del revisor)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030992
localization_priority: Normal
ms.assetid: be39cd0b-56bf-a070-f5d8-c9a440d81ee2
description: Contiene el nombre del revisor de un documento.
ms.openlocfilehash: 02f353ab8f2d39cc075211bb13157b93081e9d8f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335171"
---
# <a name="name-cell-reviewer-section"></a>Celda Name (Sección del revisor)

Contiene el nombre del revisor de un documento.
  
## <a name="remarks"></a>Comentarios

 El valor predeterminado es el nombre que se encuentra en el cuadro **nombre de usuario** de la ficha **General** del cuadro de diálogo **Opciones de Visio** (haga clic en la pestaña **archivo** , haga clic en **Opciones**y, a continuación, haga clic en **General**). 
  
Para obtener una referencia a la celda name por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Reviewer.Name [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Name por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionReviewer** <br/> |
| Índice de fila:  <br/> |**visRowReviewer** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visReviewerName** <br/> |
   

