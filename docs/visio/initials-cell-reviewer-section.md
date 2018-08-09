---
title: Celda Initials (Sección de revisor)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
localization_priority: Normal
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: Contiene las iniciales del revisor de un documento.
ms.openlocfilehash: 65f0082219c8d6adca55af86c027b2ec5642fb5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822350"
---
# <a name="initials-cell-reviewer-section"></a>Celda Initials (sección Revisor)

Contiene las iniciales del revisor de un documento.
  
## <a name="remarks"></a>Observaciones

El valor predeterminado es las iniciales en el cuadro **iniciales** de la ficha **General** en el cuadro de diálogo **Opciones de Visio** (haga clic en la pestaña **archivo** , haga clic en **Opciones**y, a continuación, haga clic en **General** ). 
  
Para obtener una referencia a la celda Initials por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Reviewer.Initials [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia a la celda Initials por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionReviewer** <br/> |
| Índice de fila:  <br/> |**visRowReviewer** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visReviewerInitials** <br/> |
   

