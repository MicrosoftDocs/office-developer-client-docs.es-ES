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
ms.openlocfilehash: 6bc1629c51fc4dcb3fe7e2d6576e8f1f096144ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822671"
---
# <a name="name-cell-reviewer-section"></a>Celda Name (sección Revisor)

Contiene el nombre del revisor de un documento.
  
## <a name="remarks"></a>Observaciones

 El valor predeterminado es el nombre que se encuentran en el cuadro **nombre de usuario** en la ficha **General** del cuadro de diálogo **Opciones de Visio** (haga clic en la pestaña **archivo** , haga clic en **Opciones**y, a continuación, haga clic en **General**). 
  
Para obtener una referencia a la celda Name por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Reviewer.Name [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Name por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionReviewer** <br/> |
| Índice de fila:  <br/> |**visRowReviewer** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visReviewerName** <br/> |
   

