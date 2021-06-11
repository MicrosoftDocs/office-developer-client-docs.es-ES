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
ms.openlocfilehash: ddca3697dfcf1f422efacbe395c18f1a6b8ac48c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411508"
---
# <a name="initials-cell-reviewer-section"></a>Celda Initials (Sección de revisor)

Contiene las iniciales del revisor de un documento.
  
## <a name="remarks"></a>Comentarios

Este valor es el valor  predeterminado de las iniciales del cuadro Iniciales de la  ficha **General** del cuadro de diálogo Opciones de **Visio** (haga clic en la pestaña Archivo, en Opciones y, a continuación, en **General** ).  
  
Para obtener una referencia a la celda Initials por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Reviewer.Initials [  *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia a la celda Initials por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionReviewer** <br/> |
| Índice de fila:  <br/> |**visRowReviewer**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visReviewerInitials** <br/> |
   

