---
title: Celda DynFeedback (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251317
localization_priority: Normal
ms.assetid: 44017319-7146-3431-e476-fbb1a40341ca
description: Cambia el tipo de efecto visual ofrecido a los usuarios cuando arrastran un conector. Al soltar el botón del mouse (ratón), la forma conector resultante no se ve afectada por esta configuración. Esta configuración no se aplica a conectores enrutables.
ms.openlocfilehash: 823b8db4dc6afe94a5fdac1f62aaa48d7e1b0d80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315746"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a>Celda DynFeedback (Sección de varios)

Cambia el tipo de efecto visual ofrecido a los usuarios cuando arrastran un conector. Al soltar el botón del mouse (ratón), la forma conector resultante no se ve afectada por esta configuración. Esta configuración no se aplica a conectores enrutables.
  
|**Value**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| comprendi  <br/> | Permanece recto (sin segmentos).  <br/> |**visDynFBDefault** <br/> |
| 1  <br/> | Al arrastrarlo, presenta tres segmentos.  <br/> |**visDynFBUCon3Leg** <br/> |
| segundo  <br/> | Al arrastrarlo, presenta cinco segmentos.  <br/> |**visDynFBUCon5Leg** <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda DynFeedback por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | DynFeedback  <br/> |
   
Para obtener una referencia desde un programa a la celda DynFeedback por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowMisc** <br/> |
| Índice de celda:  <br/> |**visDynFeedback** <br/> |
   

