---
title: Celda ConLineJumpCode (Sección de diseño de la forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
localization_priority: Normal
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: Determina cuándo salta un conector.
ms.openlocfilehash: 002f628841356ec8a22afbb9d4aeca8236058222
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821843"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a>Celda ConLineJumpCode (sección Diseño de forma)

Determina cuándo salta un conector.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |
          Según especifica la página; para ver las especificaciones de la página, en la ficha **Diseño**, haga clic en la flecha del grupo **Configurar página** y, a continuación, haga clic en la pestaña **Diseño y enrutamiento**  <br/> |**visSLOJumpDefault** <br/> |
|1  <br/> |Nunca  <br/> |**visSLOJumpNever** <br/> |
|2  <br/> |Siempre  <br/> |**visSLOJumpAlways** <br/> |
|3  <br/> |Otro conector salta  <br/> |**visSLOJumpOther** <br/> |
|4  <br/> |
          Ningún conector salta
  <br/> |**visSLOJumpNeither** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de esta celda seleccionando un conector dinámico, haciendo clic en **comportamiento** en el grupo **Diseño de formas** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, haga clic en la ficha **conector** . 
  
Para obtener una referencia a la celda ConLineJumpCode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ConLineJumpCode  <br/> |
   
Para obtener una referencia desde un programa a la celda ConLineJumpCode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
|Índice de celda:  <br/> |**visSLOJumpCode** <br/> |
   

