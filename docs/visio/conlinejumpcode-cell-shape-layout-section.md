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
ms.openlocfilehash: 28bf506b8d3729fefec438d259746661fd28586e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421623"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a>Celda ConLineJumpCode (Sección de diseño de la forma)

Determina cuándo salta un conector.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|comprendi  <br/> |Según especifica la página; para ver las especificaciones de la página, en la ficha **Diseño**, haga clic en la flecha del grupo **Configurar página** y, a continuación, haga clic en la pestaña **Diseño y enrutamiento**  <br/> |**visSLOJumpDefault** <br/> |
|1  <br/> |Nunca  <br/> |**visSLOJumpNever** <br/> |
|segundo  <br/> |Siempre  <br/> |**visSLOJumpAlways** <br/> |
|3  <br/> |Otro conector salta  <br/> |**visSLOJumpOther** <br/> |
|4   <br/> |Ningún conector salta  <br/> |**visSLOJumpNeither** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de esta celda seleccionando un conector dinámico, haciendo clic en **comportamiento** en el grupo **diseño de formas** en la ficha [programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, haciendo clic en la pestaña **conector** . 
  
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
   

